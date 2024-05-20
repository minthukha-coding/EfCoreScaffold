# EfCoreScaffold

To scaffold an Entity Framework Core context from an existing database, follow these steps:

1. Install the `dotnet-ef` tool globally (version 7):

    ```bash
    dotnet tool install --global dotnet-ef --version 7
    ```

2. Update the `dotnet-ef` tool globally to ensure you have the latest version:

    ```bash
    dotnet tool update --global dotnet-ef
    ```

3. Scaffold the DbContext and entity classes using the `dotnet ef dbcontext scaffold` command:

    ```bash
    dotnet ef dbcontext scaffold "Server=.;Database=MTKDotNetCore;User ID=sa;Password=sasa@123;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer -o Db -c AppDbContext
    ```

This command connects to the `MTKDotNetCore` database using the specified connection string and scaffolds the DbContext (`AppDbContext`) and entity classes into the `Db` directory.
