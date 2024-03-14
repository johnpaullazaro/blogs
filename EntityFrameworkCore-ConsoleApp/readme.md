


# Entity Framework Core

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

``c#
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

``

