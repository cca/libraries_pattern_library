# CCA Libraries & Instructional Technology Design Pattern

Design patterns for the libraries' 2017 website redesign.

## style.css

Right now, the styles.css file is simply a compiled version of the [CCA Portal](http://portal.cca.edu) styles. We will diverge eventually, and we won't rely on the static file sitting inside this project; the plan is to eventually have the CSS and JS that powers the pattern library (defined in the "assets" property of data.json) to be symlinks to the actual files used by the website's CMS.

## Astrum

This pattern library is built with [Astrum](http://astrum.nodividestudio.com/). It should run independently but if you install Astrum it facilitates adding components to the library.

```sh
> # install astrum globally, requires Node & npm
> npm i -g astrum
> # create a new "tacocat" component inside the "buttons" group
> astrum new buttons/tacocat
```

When a new component is created, it has a "description.md" and a "markup.html" inside a folder bearing its name which lives inside its group's folder. The description is for describing what the component is and how it's used; the markup is a _minimal_ example of its usage.

All the special sauce lives in data.json, laid out in an understandable manner. You could manually create components by mimicking an existing one's settings and file structure.
