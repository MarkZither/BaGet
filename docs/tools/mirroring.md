# Mirroring nuget.org

!!! warning
    This page is a work in progress!

## Importing packages for a solution from nuget.org
You can import all packages for a specific solution from nuget.org:
1. Navigate to a solution e.g. `.\BaGet`
2. Run:

```
dotnet restore --force --source https://your-baget-url/v3/index.json
```

## Importing specific packages from nuget.org
You can import a specific package from muget.org by calling a url like this.
https://your-baget-url/v3/registration/BaGet.Core.Server/0.2.0-preview1.json

## Importing package downloads from nuget.org

You can import package downloads from nuget.org:

1. Navigate to `.\BaGet\src\BaGet`
2. Run:

```
dotnet run import downloads
```
### How this works
1. A json file is downloaded from https://nugetprod0.blob.core.windows.net/ng-search-data/downloads.v1.json which is over 55Mb and contains all of the packages and versions on NuGet.org.
2. A list of packages currently in your database is iterated over and the download count for each package version is syncronised with the count on nuget.org.

## Indexing nuget.org

* TODO Check-in code
* Explain scaling
* Rebuild indexes at end
* Importing downloads from nuget.org
