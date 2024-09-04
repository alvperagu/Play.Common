# Play.Common
Common libraries used by Play Economy services.

## Create and publish package
```powershell
$version="1.0.7"
$owner="alvperagu"
$gh_pat="[TOKEN HERE]"
dotnet pack src\Play.Common\ --configuration Release -p:PackageVersion=$version -p:RepositoryUrl=https://github.com/$owner/Play.Common -o ..\packages

dotnet nuget push ..\packages\Play.Common.$version.nupkg --api-key $gh_path --source "github"
```