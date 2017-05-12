# CCA Libraries & Instructional Technology Design Pattern

Design patterns for the libraries' 2017 website redesign. This repository will eventually be live at http://libraries.cca.edu/static/pattern-library/index.html and included in the libraries new website repo as a git submodule.

## styles.css

Right now, the styles.css file is simply a compiled version of the [CCA Portal](http://portal.cca.edu) styles. We will diverge eventually, and we won't rely on the static file sitting inside this project; the plan is to eventually have the CSS and JS that powers the pattern library (defined in the "assets" property of data.json) to be symlinks to the actual files used by the website's CMS.

## Astrum

This pattern library is built with [Astrum](http://astrum.nodividestudio.com/). It should run independently but if you install Astrum it facilitates adding components to the library.

```sh
> # install astrum globally, requires Node & npm
> npm i -g astrum
> # create a new "tacocat" component inside the "buttons" group
> astrum new buttons/tacocat
> # edit the configuration of an existing component
> astrum edit buttons/tacocat
> # …or a group
> astrum edit --group buttons
```

When a new component is created, it has a "description.md" and a "markup.html" inside a folder bearing its name which lives inside its group's folder, e.g. "components/buttons/tacocat". The description says what the component is and how it's used on the site; the markup is a _minimal_ example of its usage.

The special sauce lives in data.json, laid out in an understandable manner. You can manually create components by mimicking an existing one's settings and file structure.
