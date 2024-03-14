


# Entity Framework Core
<br><br>



## Creating new application
### .NET CORE CLI
``
dotnet new console -o myApp
cd myApp
``
### Visual Studio 2023
1) Open Visual Studio
2) Click new project
3) Select console App
4) Enter myApp

``
install-package Microsoft.EntityFrameworkCore.SQLServer
``




## Install EF Core
### .NET CORE CLI
``
dotnet add package Microsoft.EntityFrameworkCore.Sqlite
``
### Visual Studio 2023
``
install-package Microsoft.EntityFrameworkCore.SQLServer
``

### Create a model

```csharp
  public class Blog
{
    public int BlogId { get; set; }
    public string Url { get; set; }

    public List<Post> Posts { get; } = new();
}

public class Post
{
    public int PostId { get; set; }
    public string Title { get; set; }
    public string Content { get; set; }

    public int BlogId { get; set; }
    public Blog Blog { get; set; }
}

```

