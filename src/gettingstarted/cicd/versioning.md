# Versioning

AppsDock OS uses semantic versioning based on git tags and branches. Version tags always start with a `v` followed by the semantic version `#.#.#` and one of the channels with its revision e.g. `-dev-5`.

The channel must be defined by one of the following:

    dev     Used for development builds
    beta    Used for beta builds
    rc      Used for release candidates
    stable  Used for final stable builds

Each channel, except the stable, must define the current version specific build revision right behind the channel.

Example:

    v1.4.2-dev-23       A development build with revision 23
    v3.2.7-rc-3         A release candidate build with revision 3
    v1.7.3-stable       A stable build


Both the system app (application/src/System) and any other app (application/apps) determines its own version and deployment lifecycle.
Example:

    com.appsdock.system     AppsDock OS System      v1.4.2-stable
    com.appsdock.dms        AppsDock OS App         v2.4.1-dev-3
    com.appsdock.hrm        AppsDock OS App         v0.9.3-rc-3

Each version is defined in the manifest file of each app and in the application system app.

Example appsdock/application/manifest.json

~~~json
{
    "app": {
        ...
        "version": "1.3.2",
        "channel": "dev",
        "build": "1"
    },
    ...
}
~~~

The `channel` and `build` must be set always on `dev` and `1` due to these parts will be automatically set to the right values during the CI/CD process, which reads the manifest and creates a build based on the defined version. 

## Channel Promotion

Code changes can be only build within the dev channel. If the dev build is ready for the next channel, you have to promote the latest dev revision to the next channels. 

