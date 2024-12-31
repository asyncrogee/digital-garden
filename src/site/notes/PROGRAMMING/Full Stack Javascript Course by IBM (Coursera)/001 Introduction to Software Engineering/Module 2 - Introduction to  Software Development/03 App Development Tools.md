---
tags:
  - programming
  - softwareengineering
  - softwaredevelopment
  - SDLC
dg-publish: true
Topic: Software Development
---

> [!info] Version Control
>
> - Keeps track of:
>   - What changes were made
>   - When they were made
>   - Who made them
> - Resolve change conflicts
> - Provides a way to revert to an older version
> - Examples:
>   - Git
>   - Github

> [!abstract] Libraries
>
> - **Collections of reusable code**
> - Multiple code libraries can be integrated into a project
> - Codes can be called when required
> - Can solve specific problems or add specific features
>   > [!example] Examples of code libraries are:
>   >
>   > - **jQuery**: a JavaScript library that simplifies DOM manipulation
>   > - **Email-validator**: checks if email address is correctly constructed and valid
>   > - **Apache Commons Proper**: a repository of reusable Java components

> [!abstract] Frameworks
>
> - Provides a **_standard way_** to build and deploy applications
> - **Acts as a skeleton** you extend by adding your own code
> - Should be determined and used from the beginning
> - Dictates the architecture of the app
> - Calls your code
> - Allow you **_less control than libraries_**
>
> > [!example]
> >
> > - **AngularJS** is a JavaScript-based framework for dynamic web applications
> > - **Vue.js** is a Javascript framework focused on the user interface
> > - **Django** is a framework that uses Python for web development

> [!info] Inversion of control
> ![Pasted image 20241215002356.png](/img/user/Misc/attachments/Pasted%20image%2020241215002356.png)

> [!info] CI/CD
>
> - **Continuous Integration** with **_Continuous Delivery_** or Continuous Deployment
> - Enables developers to deliver frequent changes reliably
> - Implemented through a build-automation server
> - CI automatically builds and tests code
> - CD deploys the changes

> [!info] Build Tools
>
> - Transform source code into binaries for installation
> - Important in environments with many inter-connected projects and multiple developers
> - **Automate tasks** like:
>   - Downloading dependencies
>   - Compiling source code into binary code
>   - Packaging that binary code
>   - Running tests
>   - Deployment to production systems
> - Initiate a build from the command line or from an IDE
> - Two categories that are widely used: - Build-automation **utilities** - generates build artifacts like _executables_, by compiling and linking source code - Build-automation **servers** - executes **Build-automation utilities** on scheduled or triggered basis.
>   > [!example] Some example of build tools
>   >
>   > - Webpack: a module bundler for JavaScript
>   > - Babel: a JavaScript compiler
>   > - Web Assembly: a binary instruction format that runs in your browser

> [!info] Packages
>
> - Packages make apps easy to install
> - Packages contain
>   - App files
>   - Instructions for installation
>   - Metadata
>
> > [!tip] Package managers
> >
> > - **To distribute packages**
> > - Make working with packages easier
> > - Coordinate with file archivers to extract package archives
> > - Verify checksums and digital certificates to ensure the integrity and authenticity of the package
> > - Locate, download, install, or update existing software from a software repository
> > - Manage dependencies to ensure a package is installed with all packages it requires
> >   > [!example] Package managers by platform
> >   > Some commonly used package managers for the major platforms are:
> >   >
> >   > - **_Linux_**
> >   >   - Debian Package Management System (DPKG)
> >   >   - Red Hat Package Manager (RPM)
> >   > - **_Windows_**
> >   >   - Chocolatey
> >   > - **_Android_**
> >   >   - Package Manager
> >   > - **_MacOS_**
> >   >
> >   >   - Homebrew
> >   >   - MacPorts
> >   >
> >   > - **_Cloud application_** package Managers
> >   >   - Manages Libraries and Utility Code
> >   >     - **Node.js / JavaScript**
> >   >       - npm
> >   >     - **Java**
> >   >       - Gradle
> >   >       - Maven
> >   >     - **Ruby**
> >   >       - RubyGems
> >   >     - **Python**
> >   >       - Pip
> >   >       - Conda
