# Commit messages

The commit message must begin with the type of commit, followed by any number of tags. Optionally, a note can also be specified. This must begin with a capital letter. The second and all further lines contain the changes that have taken place. One change per line. Paragraphs are not permitted; they must be written through, as a paragraph introduces a new change.

## Types

| Type | Description
| ---- | -----------
| `BUGIFX` | Error in code fixed. The note area must contain the issue (number) if available.
| `CHANGE` | Existing code changed.
| `HOTFIX` | Bug fixed at short notice, without planning and testing).
| `NEW` | New code added.
| `REFACTOR` | Reorganised existing code.
| `RELEASE` | New version released. The version number must be specified with a leading v as a tag.

## Tags

The tags must be written in Camel case format. The tags must be listed in order from general to specific.

| Tag | Description | Example
| --- | ----------- | --------
| `#component` | Changes affecting components. | components/
| `#css` | Adjustments in stylesheet files only. | .css, .sass
| `#design` | Cosmetic adjustments that only affect the appearance, but no function. | .css, .sass, .vue, ...
| `#git` | All Git files. | .gitignore
| `#middleware` | Changes that affect the middleware. | middleware/\*.js
| `#nuxt` | All Nuxt.js files. | nuxt.config.js
| `#package` | The package.json file. | package.json
| `#page` | Changes that affect pages.| page/
| `#plugin` | Changes that affect plugins. | plugin/\*.js
| `#poc` | Changes that are temporarily relevant for a proof of concept. | .\*
| `#project` | All files that are not directly related to the application. | package.json, nuxt.config.js, docker-compose.yml
| `#static` | Changes that affect static files. | static/
| `#store` | All changes that affect the store. | store/.js
| `#vuetify` | All Vuetify.js files. | vuetify.options.js

## Examples

~~~
CHANGE #plugin #css #middleware Image plugin
Add a new image plugin for test images.
Add a new static css helper file.
~~~

~~~
RELEASE #v1.12.5 Pre-Release
~~~
