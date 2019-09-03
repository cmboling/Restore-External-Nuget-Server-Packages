# Restore-External-Nuget-Server-Packages
proof of concept to learn how to restore Net Core project with packages from a private nuget server


### Solution:
https://stackoverflow.com/questions/50155496/dotnet-restore-fails-for-private-nuget-packages

You can define custom package sources in a NuGet.Config file in the root directory of your source control repository containing your source code. Then you do not need to configure it on every machine.

When you run a nuget restore solution.sln or dotnet restore solution.sln the solution's directory will be checked first for a NuGet.Config file, then the directory above, all the way back to the root directory. Finally the NuGet.Config under the user's profile will be checked.
