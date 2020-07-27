# Data First with Entity Framework Core - Specific Tables

Applies data first approach with Entity Framework Core for specific tables.

With .NET Core CLI

```bash
dotnet ef dbcontext scaffold "CONNECTION STRING" MySql.Data.EntityFrameworkCore -o PROJECT_FOLDER_WHERE_CONTEXT_WILL_BE -t actor -t film -t film_actor -t language -f
```

With Visual Studio Packager Manager Console

```powershell
Scaffold-DbContext "CONNECTION STRING" MySql.Data.EntityFrameworkCore -OutputDir PROJECT_FOLDER_WHERE_CONTEXT_WILL_BE -Tables actor,film,film_actor,language -f
```

Notes:

- _change MySql.Data.EntityFrameworkCore for any other provider in project._
- Will generate new context with database name. If wanted, can be changed with `-Context "newContextName"`.

[source](https://stackoverflow.com/questions/39065769/can-we-scaffold-dbcontext-from-selected-tables-of-an-existing-database)
