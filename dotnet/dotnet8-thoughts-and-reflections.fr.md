# .NET 8, faisons le point


.NET est parmi nous depuis le début des années 2000, ce qui fait un bon bout de temps.
Le framework a beaucoup évolué et traversé différentes "époques", "modes", contextes et changements de stratégie.
L'évolution a été telle que la version actuelle du framework est assez différente de celle de ses débuts, dans son contenu mais aussi dans sa stratégie.

Au-delà de cette transformation, on peut se demander qu'est-ce que ce framework a à nous offrir.
La question est quelque part assez naturelle.

Par ailleurs, il est assez étonnant de remarquer que malgré tous ces changements, les avis d'une certaine partie de la communauté semblent ancrés à un contexte révolu.
Cet article synthétise la nouvelle situation en essayant de rester aussi objectif que possible et invite les lecteurs à se faire un nouvel avis en ignorant tout autre avis (même celui-ci) et comprendre ce que .NET a à offrir aujourd'hui.


# Version actuelle: .NET 8

.NET 8 est la version actuelle de .NET.
Il s'agit d'une version LTS (Long Term Service), ce qui signifie que le support et les updates seront garantis et maintenus plus longtemps que pour les versions STS (Short Term Service).

.NET 8 est construit dans la continuité de la fusion de .NET Framework and .NET Core. Cette fusion a été amorcée par .NET 5 et s'enrichit de version en version.

.NET 8 est conçu pour être cross platform (Windows, Linuw et MacOS) en opposition à .NET Framework, très couplé à Windows.
.NET 7 et .NET 8 en particulier ont amené de gros progrès sur ces sujets.
Aujourd'hui, l'aspect cross-platform est assez riche sauf sur certaines des technos UI desktop. Mais il existe des solutions qui cherchent à apporter des solutions en ce sens (Blazor, MAUI même si tout n'est pas rose avec MAUI encore).

Au-delà de cet aspect cross-platform, .NET 8 a été fortement revu pour améliorer la sécurité et les performances de manière assez significative.
En effet, les librairies pour le cryptage sont désormais nettement plus cross-platform et de nouveaux modes de compilation sont en train d'être rajoutés pour améliorer drastiquement la taille des packages et les performances. En plus de la compilation, le code a été profondement revu pour le rendre plus performant à la base.

De manière similaire, la containerisation est en train d'être fortement revue et optimisée (voir plus loin pour les détails).

Vous trouverez ci-dessous une liste (non exhaustive) des axes d'amélioration les plus significatifs.


# Extract des changements ou sujets d'améioration in .NET 8


.NET couvre de spectre assez large en termes de domaines de développement.
Les sujets les plus siginificatifs sont:
 - Web development (special mention to Blazor, the framework to develop WASM apps in C#)
 - native and cross-platform mobile development (MAUI)
 - Desktop development (WPF, UWP, WinUI, MAUI) (not mentioning WinForms even though it seems still quite used)
 - Cloud development (APIs, Azure Functions, event/messages driven applications, data consuming applications, etc)
 - Containerization
 - Machine learning
 - IoT development (IoT Operations, and IoT Solutions at cloud level)
 - API development (WebAPIs, minimal APIs, CoreWCF, gRPC, etc)
 - Distributed applications (Aspire, DAPR, etc)
 - certains aspects de la gestion et accès aux données



# D'autres sujets intéressants sur .NET 8

.NET 8 est Open Source. En effet, ceci continue à surprendre encore mais .NET 8 est bien Open Source.

De même, une communauté très riche et active alimente et enrichit .NET 8.
TODO
Exemples de projets
//Rajouter des exemples de projets opensource


## L'outillage

### IDEs et interfaces de développement

L'outillage mérite de faire une section à part.

Ce dernier a également évolué avec .NET:
 - la famille complète des différentes version de Visual Studio, étant toujours un IDE exceptionnel en termes de productivité (fonctionnalité, templates, ergonomie, debugg, etc)
 - Visual Studio Code qui, même si intéressant, reste loin Visual Studio pour du développement .NET

Des éditeurs tiers se sont également faits une place, en particulier, dans la zone des IDEs cross-platform et en adressant certains types de projets (ex: Rider).

### CLI

.NET CLI est souvent mis de côté mais ce dernier est très riche.
L'une des dernières nouveautés est la possibilité de construire des images Docker directement en CLI, sans dépendre du CLI Docker et sans devoir construire des Dockerfile.



## Contenus

Les contenus disponibles en ligne (gratuits et payants) sont nombreux.
La documentation officielle (Microsoft Learn) est relativement acceptable (bien pour démarrer mais pas suffisante à mes yeux pour approfondir les sujets).
Il existe néanmoins des contenus payants de très bonne qualité pour aller plus loin (ex: [dometrain.com](dometrain.com) de Nick Chapas, Pluralsight, etc).

Apress et Packt publient également de très bons livres sur les différents sujets autour de .NET.


## Courbe apprentissage

La "simplicité" et la cohérence de .NET, la richesse des librairies, la variété des projets possibles font de .NET un framework très efficient et multiusages.
Quand on regarde l'un des sujets en particulier, la courbe d'apprentissage est relativement courte.
Quand on regarde dans l'ensemble, la courbe d'apprentissage des différents workloads reste également très raisonnable.
Ceci fait de .NET un framework à très bon ROI, ce qui est toujours bon à prendre en tant que développeur et surtout, en tant qu'entreprise.

## Besoins d'entreprise et/ou professionels

.NET répond bien aux critères de fonctionnalités techniques, usage et son aspect pratique.
Ces points sont importants mais les besoins vont souvent au-delà dans des environnements d'entreprise ou professionnels.
Qu'en est-il?

.NET offre de nos jours:
 - un niveau de maturité très avancé
 - une stabilité et qualité dans son évolution (même si la stabilité reste relative car l'écosystème évolue constamment)
 - des roadmaps claires et publiques
 - un support efficace
 - une fiabilité importante
 - des updates très fréquents pour corriger des bugs ou incrémenter la sécurité
 - une sécurité testée et améliorée constamment
 - une amélioration continue incéssante
 - une projection temporelle rassurante
 - des outils de migration quand certains changements de version exigent des upgrades importants
 - des outils de travail intégrés, efficaces, stables et performants

Ces éléments mettent .NET dans une position très robuste dans l'environnement professionnel.


## Ecosystème

La taille de l'écosystème et la/les communauté(s) est difficile à estimer.
Sans rentrer dans des considérations subjectives, l'écosystème .NET est significatif, varié et actif.

Cet écosystème est composé de:
- éditeurs tiers
- entreprises privées
- communauté composée par de nombreux développeurs
- contributeurs (MVPs, RDs, autres types de membres de la communauté, etc)


## Performances


Comme mentionné précédemment, l'amélioration des performances est un vrai sujet. Le bond en avant de .NET en ce sujet est assez impresionnant et les efforts continuent. Les nouveaux modes de compilation devraient apporter un autre niveau de gains sur cet aspect.

Au-delà du gain direct sur les temps de réponse, ceci se traduit aussi en une réduction des coûts pour les services Azure.


## EF8

Entity Framework a souvent été dans le centre de critques dues aux performances.
Il est vrai que malgré sa richesse fonctionnelle, il intégrait des axes d'amélioration dans ce chapitre (surtout pour les solutions gérant des volumes d'appel importants et avec des flux de données importants également).

D'importants travaux et améliorations ont été réalisés dans la version 8.
Ainsi, EF Core 8 redevient une solution très compétitive.


## Blazor 8

Le développement web a été un sujet sur lequel Microsoft s'est vu dépasser par différentes autres technologies.
Depuis quelques temps, Microsoft (et d'autres grands éditeurs) cherchent à radicalement changer l'expérience du développement web (coûts, retour sur investissement, fonctionnalités, possibilités, etc). Web Assembly est l'une des technologies qui semble prendre le plus de poids en tant qu'alternative/solution. Blazor est la solution de Microsoft pour créer des projets de type Web Assembly.

Microsoft a commencé à travailler dessus il y a déjà plusieurs années. Aujourd'hui, Blazor 8 commence à atteindre un niveau de matûrité et performances intéressants. Le niveau de mâturité inclut aussi les outils de développement.
Il reste encore des axes d'amélioration mais l'alternative est de plus en plus sérieuse.


## Développement API

Le développement d'APIs est dévenu inévitable et vital de nos jours.

.NET apporte également beaucoup de richesse sur ces aspects (peut-être plus que partout ailleurs):
 - REST APIs basées sur WebAPI (controller-based development)
 - minimal APIs
 - gRPC
 - CoreWCF
 - containerisation
 - monitoring et governance (standards comme Open Telemetry)
 - first class resilience mechanisms
 - YARP
 - les nombreux templates pour Visual Studio et/ou .NET CLI
 - l'expérience de debug
 - http/rest files
 - etc


# Application distribuées

Le sujet naturel après le développement de services est surement le développement d'applications distribuées.

.NET offre une richesse de possibilités très intéressante également sur cet aspect. Combiné à Azure, le duo devient très attractif:
 - Azure App Service (containerized or not)
 - Azure Container for Apps (ACA)
 - Azure Kubernes Service (AKS)
 - APIM
 - Azure Container Registry (ACR)
 - Azure Monitor
 - All the security services related to the services mentioned above

Mention spéciale à Aspire, nouveau projet de Microsoft, lié à .NET, pour développer des solutions distribuées.
https://learn.microsoft.com/en-us/dotnet/aspire/get-started/aspire-overview?WT.mc_id=AZ-MVP-5004280

L'initiative a eu un tel accueil et engougement que le sujet est en train d'évoluer très répidement.

D'autres projets comme Dapr, Orleans, Radius se penchent sur ces problématiques d'applications distribuées.


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