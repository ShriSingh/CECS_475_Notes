.NET Standard Library is intended to be available on all .NET runtimes
- Best way to build a cross-platform class library
- Multiple versions to consider that are available to varying degrees across right platforms
	- If a project targets a lower version, it cannot reference a project that targets a higher version
		- Pick the lowest possible .NET Standard version to use across all projects

External Links:
- [Port from .NET Framework to .NET 7 - .NET Core | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/core/porting/#targeting-the-net-standard-library)