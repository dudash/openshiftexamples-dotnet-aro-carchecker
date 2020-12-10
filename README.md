# CarChecker on ARO
[![OpenShift Version][openshift-heximage]][openshift-url]

## an ASP .NET Core Blazor sample app running in Azure Red Hat OpenShift
This is a sample application for [Blazor](https://blazor.net) which was presented at Build 2020.  I've tweaked some things in order to showcase it running in Azure Red Hat OpenShift (ARO). The original source for this application can be found here: [https://github.com/SteveSandersonMS/CarChecker][2].

* You can view the on-demand walk-through for the original CarChecker app on Channel 9: [Modern Web UI with Blazor WebAssembly][3].
* You can view an on-demand overview of the changes I made and me running through some CI/CD for the app in OpenShift [here](here).

## What this sample app has:
This is a great sample which has a lot of Blazor + ASP.NET integrations such as:
- client-side debugging with Visual Studio 
- Authentication / Authorization
- input validation
- data integration/sync
- Blazor components
- code sharing
- JavaScript interop
- Localization / internationalization
- Progressive Web App (PWA)

## What ARO provides:
- Reduce operational overhead and focus on quickly delivering applications
- .NET Core source-2-image (s2i) which containerizes the app for us
- deploy applications in a consistent environment
- Secured and patched base container images for .NET 
- Ability to trigger build/deploy and pipelines (from code change and other triggers)


## How to run this thing
### Deploy to OpenShift (Server)
> Note: If you don't already have an ARO cluster and you want to learn how to create one, check out some instructions [here](https://docs.microsoft.com/en-us/azure/openshift/tutorial-create-cluster).

By simply adding a .s2i/environment file to this repo, I let OpenShift know which .csproj to deploy. You can easily containerize and run this app using Azure Red Hat OpenShift (ARO). If you want to deploy this app to your cluster, it's as simple as using the oc CLI command `oc new-app` or the plus button in the ARO web console.

### Running for development
We can use `dotnet` tooling to run locally. And for a nice combination of local + ARO testing get the [odo CLI](https://odo.dev/) tool the `odo push` command (or [VSCode plugin](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-openshift-connector)).

## Build Code, Containers, Scan, and more in a Pipeline
We can put this app into a larger release flow example using pipelines. You can see that in action by doing the following:
TBD


[1]: https://docs.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-3.1#blazor-webassembly
[2]: https://github.com/SteveSandersonMS/CarChecker
[3]: https://aka.ms/blazor-in-action

[openshift-heximage]: https://img.shields.io/badge/ARO-4-BB261A.svg
[openshift-url]: https://docs.openshift.com/aro/4/welcome/index.html
