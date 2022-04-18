# Dependency Injection
A dependency is an object that another object depends on. Examine the following MyDependency class with a WriteMessage method that other classes depend on:

```
public class MyDependency
{
    public void WriteMessage(string message)
    {
        Console.WriteLine($"MyDependency.WriteMessage called. Message: {message}");
    }
}
```


### Dependency injection addresses these problems through:

* The use of an interface or base class to abstract the dependency implementation.

* Registration of the dependency in a service container. ASP.NET Core provides a built-in service container, IServiceProvider. Services are typically registered in the app's Program.cs file.

* Injection of the service into the constructor of the class where it's used. The framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.

### By using the DI pattern, the controller or Razor Page:

* Doesn't use the concrete type MyDependency, only the IMyDependency interface it implements. That makes it easy to change the implementation without modifying the controller or Razor Page.

* Doesn't create an instance of MyDependency, it's created by the DI container.

## Service lifetimes
>To use scoped services in middleware, use one of the following approaches:


* Inject the service into the middleware's Invoke or InvokeAsync method. Using constructor injection throws a runtime exception because it forces the scoped service to behave like a singleton. The sample in the Lifetime and registration options section demonstrates the InvokeAsync approach.

* Use Factory-based middleware. Middleware registered using this approach is activated per client request (connection), which allows scoped services to be injected into the middleware's constructor.


>There are basically two types of services in ASP.NET Core:

1. Framework Services: Services which are a part of ASP.NET Core framework such as IApplicationBuilder, IHostingEnvironment, ILoggerFactory etc.
2. Application Services: The services (custom types or classes) which you as a programmer create for your application.

## Understanding Service Lifetime
Built-in IoC container manages the lifetime of a registered service type. It automatically disposes a service instance based on the specified lifetime.

The built-in IoC container supports three kinds of lifetimes:

1. Singleton: IoC container will create and share a single instance of a service throughout the application's lifetime.
2. Transient: The IoC container will create a new instance of the specified service type every time you ask for it.
3. Scoped: IoC container will create an instance of the specified service type once per request and will be shared in a single request.

## The Repository pattern
Repositories are classes or components that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer. If you use an Object-Relational Mapper (ORM) like Entity Framework, the code that must be implemented is simplified, thanks to LINQ and strong typing. This lets you focus on the data persistence logic rather than on data access plumbing.

