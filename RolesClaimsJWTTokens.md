# Roles, Claims and JWT Tokens

## Claims-based authorization in ASP.NET Core :
When an identity is created it may be assigned one or more claims issued by a trusted party.
A claim is a name value pair that represents what the subject is, not what the subject can do. 

### Adding claims checks
>Claim based authorization checks:

* Are declarative.
* Are applied to Razor Pages, controllers, or actions within a controller.
* Can not be applied at the Razor Page handler level, they must be applied to the Page.

```
var builder = WebApplication.CreateBuilder(args);

builder.Services.AddRazorPages();
builder.Services.AddControllersWithViews();

builder.Services.AddAuthorization(options =>
{
   options.AddPolicy("EmployeeOnly", policy => policy.RequireClaim("EmployeeNumber"));
});

var app = builder.Build();

if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Error");
    app.UseHsts();
}

app.UseHttpsRedirection();
app.UseStaticFiles();

app.UseAuthentication();
app.UseAuthorization();

app.MapDefaultControllerRoute();
app.MapRazorPages();

app.Run();
```

## The difference between Authentication and Authorisation

First of all, we should clarify the difference between these two dependent facets of security. The simple answer is that Authentication is the process of determining who you are, while Authorisation revolves around what you are allowed to do, i.e. permissions. Obviously before you can determine what a user is allowed to do, you need to know who they are, so when authorisation is required, you must also first authenticate the user in some way.

## JWT Authentication
JSON Web Token (JWT) is a means of representing claims to be transferred between two parties. The claims in a JWT are encoded as a JSON object that is digitally signed using JSON Web Signature (JWS) and/or encrypted using JSON Web Encryption (JWE).

>This is the second part of the series of two shorts post regarding the practical application of JWT.

* JWT for downloading the files at the client.
* JWT for the server to server authentication (current blog post).

>This blog post includes the below topics in detail:

* Parts of JWT token.
* How to authenticate servers API’s (producer and consumer concept).

