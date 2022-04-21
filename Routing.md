# Routing 

When you create a new ASP.NET MVC application, the application is already configured to use ASP.NET Routing. ASP.NET Routing is setup in two places.

## There are four sections in the configuration file that are relevant to routing :

 * the system.web.httpModules section.
 * the system.web.httpHandlers section.
 * the system.webserver.modules section. 
 * the system.webserver.handlers section.

**Be careful not to delete these sections because without these sections routing will no longer work.**

and more importantly, a route table is created in the application's Global.asax file. The Global.asax file is a special file that contains event handlers for ASP.NET application lifecycle events. The route table is created during the Application Start event.


### The Default route maps this URL to the following parameters:

- controller = Home

- action = Index

- id = 3

`/Home/Index/3`


## HomeController class

the HomeController class includes a method named Index() that accepts a single parameter named Id. The URL /Home causes the Index() method to be called with an empty string as the value of the Id parameter.


```
[HandleError]
    public class HomeController : Controller
    {
        public ActionResult Index(string id)
        {
            return View();
        }
    }
``` 

## Routing in ASP.NET Core

>Apps can configure routing using :

* Controllers
* Razor Pages
* SignalR
* gRPC Services
* Endpoint-enabled middleware such as Health Checks.
* Delegates and lambdas registered with routing.

### All ASP.NET Core templates include routing in the generated code. Routing is registered in the middleware pipeline in Startup.Configure.

```
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    if (env.IsDevelopment())
    {
        app.UseDeveloperExceptionPage();
    }

    app.UseRouting();

    app.UseEndpoints(endpoints =>
    {
        endpoints.MapGet("/", async context =>
        {
            await context.Response.WriteAsync("Hello World!");
        });
    });
}
```

> Routing uses a pair of middleware, registered by UseRouting and UseEndpoints:

* UseRouting adds route matching to the middleware pipeline. This middleware looks at the set of endpoints defined in the app, and selects the best match based on the request.

* UseEndpoints adds endpoint execution to the middleware pipeline. It runs the delegate associated with the selected endpoint.


