# .NET 8, faisons le point


.NET est parmi nous depuis le début des années 2000, ce qui fait un bon bout de temps.
Le framework a beaucoup évolué et traversé différentes "époques", "modes", contextes et changements de stratégie.
L'évolution a été telle que laa version actuelle du framework est assez différente de celle de ses débuts, dans son contenu mais aussi dans sa stratégie.

Au-delà de cette transformation, on peut se demander qu'est-ce que ce framework a à nous offrir.
L'idée de cet article est de faire un peu le bilan et ajouter une perspective depuis le monde de l'entreprise.


.NET has been around for a while, going through different levels of evolutions, growth and maturity.
It is quite fair to say that .NET is following a total new strategy line since .NET Core, and especially after the unification of.NET 5.

What seems strange is that, even though .NET has been evolving, some opinions seem to remain attached to experiences in the past.
This post shares some personal thoughts (but trying to remain as objective as possible) and invites readers to ignore all the opinionated contents (even this one) to just give a try to the current version of .NET.


# Current .NET version: .NET 8

.NET 8 is the current version of .NET.
It is a cross platform framework in contrast to .NET Framework.
Indeed, .NET Framework was tightly linked to Windows.

Besides this aspect, .NET covers now a lot of more areas, more efficiently and better.
You will find below some of them (not an exhaustive list).


# An excerpt of the changes/improvements in .NET 8

.NET 8 is a cross-platform framework that covers different workloads, such as:
 - Web development (special mention to Blazor, the framework to develop WASM apps in C#)
 - native and cross-platform mobile development (MAUI)
 - Desktop development (WPF, UWP, WinUI, MAUI) (not mentioning WinForms even though it seems still quite used)
 - Cloud development (APIs, Azure Functions, event/messages driven applications, data consuming applications, etc)
 - Machine learning
 - Game development
 - IoT development (IoT Operations, and IoT Solutions at cloud level)
 - API development (WebAPIs, minimal APIs, CoreWCF, gRPC, etc)
 - Distributed applications (Aspire, DAPR, etc)
 - C# itself
 - compilation improvements, modes, AOT, etc
 - containerization and chiseled containers
 - etc


# Other important/interesting Aspects to consider about .NET 8


## Open source

.NET is opens source.

## Community

There is an important community around .NET contributing and enriching with valuable content, libraries, tools, etc.
The number of interesting/good GitHub projects related to .NET are considerable.

## Tooling

Tooling around .NET is probably among the best in the industry.
There are proprietary IDEs like Visual Studio, Rider, etc.

There are also free IDEs like Visual Studio Code, Visual Studio Community, etc.

The same IDE is used for the different types of development.

Visual Studio, my personal choice for most of the tasks, is truly a great IDE:
 - the developer experience is quite good (IntelliSense, tools, extensions, performance analyzers, thread analyzers, etc)
 - the debugging experience is unique.
 - seamless integration with Azure, GitHub, Azure DevOps, etc (Git integration could be better though)
 
Visual Studio Code developing and debugging experience remains limited compared to Visual Studio (when it comes to .NET developement).
This said, it is growing in popularity because it addresses other needs and it is cross-platform (also free).

Rider is probably the most known alternative to Visual Studio and it is truly cross-platform.


## Learning curve

The Learn Team is working continuously to refresh, update and improve all the official learning content from Microsoft.
Microsoft Learn includes getting started tutorials, richer step by step tutorials or very detailed documentation.
These resources are free.

There are also very good paid trainings from community members (ex: [https://dometrain.com](dometrain.com) from Nick Chapsas) or profesionnal training services (Pluralsight or professional trainers).

Some books are also excellent too.

.NET learning curve is in the end, one among the most competitive ones and with a very valuable ROI.
This point is a key en companies.


## Enterprise/architectural/developer needs

Technical features and usability are one thing, but architectural/developer needs at enterprise level are another thing.
From this perspective, .NET and its whole ecosystem offer a good choice thanks to:
 - the maturity level
 - clear roadmaps (even though we all hate the speed of changes sometimes) guaranteed by a company like Microsoft
 - continuous improvements
 - reliability and stability
 - proprietary tooling that clearly improves the developer experience (coding, testing, efficiency, etc)
 - security patches and improvements
 - constant performance improvements
 - efficient support (different levels of support depending on the needs)
 - projection in time (long term support)
 - migration tools, guidance and support
 
From the business perspective, this puts .NET in a strong position.


## Ecosystem

The size of the ecosystem is hard to assess. There are probably other ecosystems larger in volume.
This said, the .NET ecosystem is quite rich in terms of variety and volume (rich enough at least to avoid the closeness feeling).

That ecosystem relies on:
 - third editors
 - private companies
 - community
 - contributors (MVPs, RDs, other community members, etc)


## Performances

Performance improvements since .NET 5 are being quite impressive actually.


## EF8

Entity Framework Core is quite convenient to use and answers to most of needs.
However, some alternatives were more performant at some specific tasks.

With .NET8, the gap between EF8 and its alternatives has been narrowed considerably.


## Blazor 8

Web development is a very special type of development.
The issues related to technologies like Javascript and the frameworks/products on top of it have been growing.

WASM tries to bring a more efficient and productive alternative (with more potential too and technologically at another level of possibilities). Blazor is Microsoft's answer to this.

Blazor is considered as a potential game changer by part of the Web Developers.


## API developement

Backend development has also seen many changes. These are the most significant:
 - REST APIs based on WebAPI (controller-based development)
 - minimal APIs
 - gRPC
 - CoreWCF
 - their monitorization, and governance (OpenTelemetry integration, custom metrics, etc generic to .NET, not only API development)
 - first class resilience mechanisms
 - YARP

The API development experience has changed considerably.
It is way easier now to focus on the business side of the code relying on homogeneous and easy to use technical layers implementing the necessary plumbing to build enterprise ready solutions.


# Distributed applications

After thinking of services, the natural next step is to think of distributed applications.
From this perspective, .NET has also evolved and gained in maturity (new containers with optimized composition, container integration, distributed logs, etc). .NET with Azure offer pretty impressive capabilities in this field:
 - Azure App Service (containerized or not)
 - Azure Container for Apps (ACA)
 - Azure Kubernes Service (AKS)
 - APIM
 - Azure Container Registry (ACR)
 - Azure Monitor
 - All the security services related to the services mentioned above

Azure is not linked to .NET only. However, it was worth it to mention the multiplied potential of combining both.

Besides these native features, there are initiatives like Dapr, Orleans, and many other that extend the alternatives of building distributed applications with .NET.

.NET 8 has also been released with Aspire, a new type of projects to address common and repetitive problems when it comes to developing distributed applications (containerized or not). Aspire is still in preview but looks very promising.


## MAUI 8

Microsoft's attempts of building tools for mobile development have not always been successful.

MAUI comes as the next step of many of them.
MAUI 8 has been delivered with the promise of solving the issues of the initial version of MAUI.

MAUI is often linked to mobile development. However, it can beyond that with cross-platform development for mobile and desktop applications.


## Traces, logging, and debugging

Good and consistent monitoring is vital in nowadays applications.
.NET brings that level of first class level of consistency. Additionnally, it can be extended to be used with other protocols or tools promoted by the community (Prometheus, OpenTelemetry, Grafana, etc).


# Bottom line

All this is only a very small portion of what .NET is today. The general development experience is soft, efficient, with less frictions than ever.
It seems .NET is not only a great technical alternative but also, a business one.

With all this is combined with Azure, DevOps (Azure DevOps, GitHub, whatever), communities and the whole ecosystem, isn't it a great time to be a .NET developer?