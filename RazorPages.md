# Razor Pages
MVC developers want probably ask why we need one more way to build web sites on ASP.NET Core? Isn’t MVC enough? From information I have found from public space I found the following reasoning:

* It’s easier to get to web development for beginners as Razor pages are more lightweight than MVC. Besides beginners there are people who are coming from other scripting languages be it old ASP or PHP or something else.

* Razor Pages fit well to smaller scenarios where building controllers and models as separate classes is overkill.
### Create a Razor Pages project
in `Startup.cs` in `ConfigureServices` :

```c#
builder.Services.AddRazorPages();
```
in `Startup.cs` in `Configure` :
```c#
app.MapRazorPages();
```

## Prerequisites
* Basic knowledge Asp. Core
* C#
* Html
* CSS

Advantages of Razor Pages
 
1. It supports cross-platform, hence it can be deployed on Windows, Unix, and Mac operating systems.
2. It is easy to learn.
3. Lightweight and flexible framework so it can fit with any application you want to build.
4. Can work with C# programming language with Razor markup.
5. More organized with code behind page like asp.net web forms.

## Who should use Razor Pages? link
Razor Pages is suitable for all kinds of developers from beginners to enterprise level. It is based on a page-centric development model, offering a familiarity to web developers with experience of other page-centric frameworks such as PHP, Classic ASP, Java Server Pages, ASP.NET Web Pages and ASP.NET Web Forms. It is also relatively easy for the beginner to learn, and it includes all of the advanced features of ASP.NET Core (such as dependency injection) making it just as suitable for large, scalable, team-based projects.

## How to get Razor Pages link
Razor Pages is included within .NET Core from version 2.0 onwards, which is available as a free download as either an SDK (Software Development Kit) or a Runtime. The SDK includes the runtime and command line tools for creating .NET Core applications. The SDK is installed for you when you install Visual Studio 2017 Update 3 or later. The runtime is used to run .NET Core applications. The Runtime-only installation is intended for use on machines where no development takes place.

## Why should you use Razor Pages? link
If you want a dynamic web site, that is one where the content is regularly being added to, you have a number of options available to you. You can use a Content Management System (CMS), of which there are many to choose from including WordPress, Umbraco, Joomla!, Drupal, Orchard CMS and so on. Or you can hire someone to build a suitable site for you. Or you can build your own if you have an interest in, and an aptitude for programming.

If you choose to build your own, you can choose from a wide range of programming languages and frameworks. If you are a beginner, you will probably want to start with a framework and language that is easy to learn, well supported and robust. If you are considering making a career as a programmer, you probably want to know that the skills you acquire while learning your new framework will enhance your value to potential employers. In both cases, learning C# as a language and ASP.NET Core as a framework will tick those boxes. If you are a seasoned developer, the Razor Pages framework is likely to add to your skillset with the minimum amount of effort.


## What about the MVC Framework? link
You can still choose to use ASP.NET Core MVC to build your ASP.NET Core web applications. If you are porting an existing .NET Framework MVC application (MVC5 or earlier) to .NET Core, it may well be quicker or easier to keep with the MVC framework. However, Razor Pages removes a lot of the unnecessary ceremony that comes with the ASP.NET implementation of MVC and is a simpler, and therefore more maintainable development experience.

The key difference between Razor Pages implementation of the MVC pattern and ASP.NET Core MVC is that Razor Pages uses the Page Controller pattern instead of the Front Controller pattern.

Razor Pages is the default for building server-side web applications in ASP.NET Core. Components within the underlying MVC framework still have their uses such as using controllers for building RESTful APIs.