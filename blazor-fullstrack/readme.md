# Blazor Fullstack Development 

## What is Blazor?
1. Frontend web framwework for .NET
2. Part of ASP.NET Core
3. Powerful reusable component model
4. has built in components
5. Build
6. rich tooling vs studio and vs code with Hot Reload
7. Write code using C#, and interop JS as needed

Blazor allows developer fto build faster web apps

## Blazor in DOTNET 8
1. Has advance server side
2. Enhance navigation and form handling
3. Streaming rendering
4. Enable interactivity


## Static Server Side Rendering ( SSR )
.NET APP < ---- > BROWSER 

### what is SSR?
no web socket.
no neeed to download web assembly files
presenting information, read only public website. 
navigation links 
forms 
not good in rich interactivity
not good in realtinme updates

.NET 3.8+                |    .NET 8
Server / Web Assembly  global interactivity   |  SSR, per page/ component interactibvity


@attribute [Streaming Rendering]
blazor knows, all tasks, and send

FEATURES OF SSR

Good - Allows you to fast initial ui/render update , 123456
Good - Begin loading static resources in parallel
Requires UI Design to make sense. 


## Enhanced Navigation
Feel faster , get a SPA like without needing a SPA
Few http request
Retain most DOM Elements 
Enable/Disable on any DOM subtree


Demo
home --> about
about  -->home 
``RETAINING DOM
<code data-permanent>
    html retained
</code>
``







