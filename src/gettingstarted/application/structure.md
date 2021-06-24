# Structure

The top level structure of AppsDock OS consists of four parts:

    - Application sources
    - Application filesystem data
    - Binaries / CLI for the interaction with the application
    - Vendor dependencies managed by composer

## Application sources
The main application source is located in the application folder of AppsDock OS. The application itself is divided into multiple parts:

    - Application main source 
    - Apps (AppsDock OS based Applications, applications build on top of AppsDock)
    - Integrations (AppsDock OS Integrations, external services integrated into AppsDock via interfaces)

### The application source composition
The application source has a unified structure which is not only used by the main application but also by all apps (AppsDock OS based Applications). This structure consists of the following parts:

    - src
    - setup
    - config
    - locales
    - docs
    - manifest

#### src
The application source contains all object-oriented classes organized in a multi layered architecture, clean code and SOLID fashion. The main application source consists - differently than in apps - of the following parts: 

    - Console
    - Core
    - System 

Thereby, System is organized in a unified fashion which is used also by all apps. Core and Console are application main specific implementations.

#### setup
The setup directory provides files which are necessary for the installation. This includes the following files:

    - database table definition files
    - tables seeding files
    - presets used for presetting system tables

#### config
The config directory contains runtime configurations. Here you can find the following parts:

    - ORM files used by doctrine for write operations
    - constants.php for defining application specific constants
    - container.php which configure the dependency injection
    - domain-events.php which registers the domain event handlers
    - integration-events.php which defines async and cross-context/application event handlers
    - system-events.php which defines the event listeners for system internal events

#### locales
This directory contains the locale (gettext based) .po files. These files are used to compile the .mo files during the installation and update.

#### docs
This directory contains technical organized documentation in php which are used both as code inline reference for exceptions/api definition and for dynamic documentation generation for the online docs. The implementation of these docs are required for implementing exceptions and rest api endpoints in AppsDock.

#### manifest
The manifest is a JSON encoded file always located in the top level directory of the application / app directory. The manifest.json is used by the main application (System) and all apps. It provides meta information about the application like a unique ID, name, version and in additional defines the dependencies which are used by composer. 

