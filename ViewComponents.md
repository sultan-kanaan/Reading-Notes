# View Components

View components are similar to partial views, but they're much more powerful. View components don't use model binding, they depend on the data passed when calling the view component. This article was written using controllers and views, but view components work with Razor Pages.

**A view component:**

* Renders a chunk rather than a whole response.
* Includes the same separation-of-concerns and testability benefits found between a controller and view.
* Can have parameters and business logic.
* Is typically invoked from a layout page.

>View components are intended anywhere reusable rendering logic that's too complex for a partial view, such as:

* Dynamic navigation menus
* Tag cloud, where it queries the database
* Sign in panel
* Shopping cart
* Recently published articles
* Sidebar content on a blog
* A sign in panel that would be rendered on every page and show either the links to sign out or sign in, depending on the sign in state of the user

**A view component consists of two parts:**

1. The class, typically derived from ViewComponent
2. The result it returns, typically a view. 

## Writing A Simple View Component
Let's implement a simple dynamic navigation menu as a view component. We want to be able to display different navigation items based on some conditional logic (e.g. the user's claims or the hosting environment). Like controllers, view components must be public, non-nested, and non-abstract classes that either …

* derive from the ViewComponent class,
* are decorated with the [ViewComponent] attribute, or
* have a name that ends with the "ViewComponent" suffix.

We'll choose the base class approach because ViewComponent provides a bunch of helper methods that we'll be calling to return and render a chunk of HTML. In a folder named "Components", we'll create a new C# class:

```C#
public class Navigation : ViewComponent
{

}
```
If you'd rather make the view component even more explicit by appending the "ViewComponent" suffix to the class name, you can additionally decorate the class with the ViewComponent attribute to specify an unsuffixed component name:

```C#
[ViewComponent(Name = "Navigation")]
public class NavigationViewComponent : ViewComponent
{

}
```

We'll also add a special Invoke method that returns an IViewComponentResult to be rendered. Similar to MVC controllers, the Content helper method handed down from the ViewComponent base class accepts a string and simply returns its value:
```C#
public IViewComponentResult Invoke()
{
    return Content("Navigation");
}
```

Another method provided by the ViewComponent class is Json, which serializes a given object and returns its JSON representation. And then, there's View, which we'll look at in a minute, but first, let's see how we can render our view component.


## View component methods
A view component defines its logic in an:

* InvokeAsync method that returns Task<IViewComponentResult>.
* Invoke synchronous method that returns an IViewComponentResult.