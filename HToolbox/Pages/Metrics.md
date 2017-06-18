#  Changeability

allReady is somewhat unique in the sense that it favors being available and reliable at times of need, but does not require often and quick delivery with short cycles of developing as most software products do.

Unlike others, allReady has no traditional clients in the sense of day-to-day consumers. On the other hand, once the product is required it better be as reliable as pen and paper and almost as easy to use.

To make sure that the product is robust, &#39;Dev&#39; and &#39;live&#39; sites are both deployed with a production-like environment thus achieving testing on an environment that is as close as possible to real-life situations.

### **Standardization**

Code for this project is contributed mainly via GitHub, as an open source project, or by dedicated hackathons. While GitHub being a great way for monitoring and sharing code – it possesses challenges as far as it goes for keeping code quality and standardization across the solution.

To face the challenges above allReady has come up with some clear policies and guide lines for:

1. [How changing the DB is handled](https://github.com/HTBox/allReady/wiki/Entity-Framework-Core-Migration-Workflow)(using EF Core migrations).
2. [Work with git](https://github.com/HTBox/allReady/blob/04456b9816ce918376e12d99c78bf434a444fed8/docs/git/gitprocess.md). Including:  
    a. Keeping main local branch in sync with the main branch on git.  
    b. Finding an issue to work on &amp; taking ownership on it using a comment  
    c. Creating a dedicated branch for the issue.  
    d. Preforming a local merge for with main branch, and resolve conflicts if required.  
    e. Creating a pull request.  
3. [Validating code correctness](https://github.com/HTBox/allReady/blob/04456b9816ce918376e12d99c78bf434a444fed8/docs/git/gitprocess.md#sending-changes-to-github) using [ver 1000 unit tests](https://github.com/HTBox/allReady/blob/04456b9816ce918376e12d99c78bf434a444fed8/docs/prerequisite_install_guide/prerequisite_install_guide.md#running-test-cases).

[Testing UI changes](https://github.com/HTBox/allReady/blob/04456b9816ce918376e12d99c78bf434a444fed8/docs/prerequisite_install_guide/prerequisite_install_guide.md#ui-tests) (using [Canopy](http://lefthandedgoat.github.io/canopy/index.html))

## _Evolution required Qualities_

| _ **Requirement** _ | _ **How Met** _ |
| --- | --- |
| _ **1.        The app must be easy to maintain cross-platform** _ | _The app is built using Xamarin – thus ensuring having maximum of shared code between multiple platforms_ |
| _ **2. Avoid database update conflicts** _ | _Updates to the database are done using EF Core migrations. Before creating a pull request – it should be tested on a clean checkout of master branch._ |

# Design metric tools

Since having many contributors, and being a non-trivial, non-small project – it seems that it could have some benefits from code metrics and CI tools such as [Code Climate](https://codeclimate.com/) and [Codebeat](https://codebeat.co/) For static code analyses and getting code metrics and estimations for code quality, especially for pull requests from contributors.

However, keep in mind that HTBox is a nonprofit, volunteering based organization, and as such – probably does not have a budget for acquiring tools.

On the up side – Htbox is backed by   [Microsoft philanthropies](https://www.microsoft.com/en-us/philanthropies) which provides services on [Azure](https://azure.microsoft.com/) (Microsoft&#39;s Cloud services platform).

Using Azure&#39;s App Service – one can implement [continues integration and deployment with integration to a GitHub repository.](https://docs.microsoft.com/en-us/azure/app-service-web/app-service-continuous-deployment) Since for HTBox Azure services are given for free, for a certain extent, this option seems appealing.

Another advantage that HTBox gets from being a volunteering organization is that many developers already have tools installed on their develop machines and may use it for their side project as well.

Based on the &#39;.gitignore&#39; file, it seems that at least some of allReady developers uses the [dotCover](https://www.jetbrains.com/dotcover/) tool for getting fast feedback on test failure and realizing in real time to what extent their code is covered with unit tests in a statement-level

Eventually, For CI, allReady admins decided to use [AppVeyor](https://www.appveyor.com/). Every pull request triggers a CI build (compile and run unit tests). This workflow gives more confidence that the code being merged to master isn&#39;t breaking anything. It seems that the main reason to go with AppVeyor [was the existing skillsets of contributors](https://github.com/HTBox/allReady/issues/94).

## Availability and Resilience



| _ **Requirement** _ | _ **How Met** _ |
| --- | --- |
| _ **1.        There should be no single point of failure** _ | _The service is hosted By Azure which offers distributed and scalable services._ |
| _ **2. The service must be available on demand in times of need** _ | _To avoid the overhead of a full deployment chain – the service is hosted by Azure. This allows the service to be up constantly on one hand and avoiding the price of maintaining a server on the other hand (using auto-scale provided by Azure)_ |
| _ **3. New contributions should not brake old features** _ | _There is a test suit that contains over 1000 tests. Contributors are encouraged run them and new ones for any new contribution.__Every pull request_ triggers a CI build (compile and run unit tests). This gives more confidence that the code being merged to master isn&#39;t breaking anything. |
| _ **4.  The service should function also when there is no reliable internet connection** _ | [Messages are being using &quot;post&quot;](https://github.com/HTBox/allReady/issues/186) _(rather than &quot;get&quot;) for utilizing connection while available – even for a brief moment.__In addition – the cellular network is being used as well for sending messages._ |
