# Modern Slavery UK Local Authorities

Exports a list of UK Local Authorities to be used in the modern slavery app.

Can be used with the [Typeahead Aria](https://github.com/UKHomeOffice/typeahed-aria), which is exported with [HOF Frontend Assets](https://github.com/UKHomeOfficeForms/hof-frontend-assets).

## Example Usage

The following is an example of Modern Slavery UK Local Authorities in a HOF `field` with Typeahead Aria:
```
'country-select'-step: {
  mixin: 'select',
  className: ['typeahead', 'js-hidden'],
  options: [''].concat(require('ms-uk-local-authorities')),
  legend: {
    className: 'visuallyhidden'
  },
  validate: ['required']
},
```

## Version Control

We follow the version format of Major.Minor.Patch i.e. (v1.2.3) where Major = breaking change, Minor non-breaking change but more than a patch, like a new feature and a Patch = non breaking usually a bugfix.


## Creating a Release <a name="creating-a-release"></a>

1) Update the version number in the package.json file. E.g.
```
"version": "1.2.3",
```

Once this PR has been approved and merged to master we follow the next steps in order to Create a release tag.

2) Tag the new module version

Once the PR has been approved and merged, let the module build and update the master branch on your local machine:

Then tag the module with the git tag command, for example:
```
git tag v5.1.1
```

Once tagged, push the new tags to the remote git server:
```
git push origin --tags
```

3) The following steps will publish to npm, please consult this page for most up-tp-date steps. 

https://collaboration.homeoffice.gov.uk/display/CTO/Updating+a+HOF+dependency+and+consuming+it+in+your+application







