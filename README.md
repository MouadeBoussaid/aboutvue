## What is Vue?

> Vue is a **progressive framework** for building user interfaces. It is designed from the ground up to be incrementally adoptable, and can easily scale
> between a library and a framework depending on different use cases. It consists of an approachable core library that focuses on the view layer only, and an
> ecosystem of supporting libraries that helps you tackle complexity in large Single-Page Applications.

### What does that mean?

- Views are pure HTML combined with Javascript expressions {{ }} and directives comparable with Angular. ngFor == v-for. Makes use of a virtual DOM like React
- Works with a single file component principle. HTML, JS and CSS in a single Vue.component file
- Reactivity system based on ES6 Proxies (since v3, v2 uses Object.defineProperty/Getters/Setters)
- Tightly integrated and well maintained ecosystem.
  - vuex
  - vue-router
  - vue-cli (wow!)
  - vue-devtools (chrome addon)
  - many more
- Has many control libraries such as Vuetify, Quasar, Element UI, Bootstrap, Vue Material, UI5 webcomponents...
- Support for Typescript (improved in v3)

### Vue / SAP UI5

- Opiniated frameworks
- Two-way binding
- Vue is very light weight (core is 10kb) , whereas UI5 is not.
- Vue has many controls just like UI5, however less business controls
- Vue is 100% opensource
- Performance difference

## What will we be doing?

| Topic               | Description          | Branch                     |
| ------------------- | -------------------- | -------------------------- |
| [Intro to Vue]      | Intro to Vue         | master                     |
| [Components]        | Intro to SFC         | components                 |
| [Exercise]          | Small exercise       | components_exercise        |
| [Exercise solution] | Solution to exercise | components_exercise_result |

## Documentation

[vuejs.org](https://vuejs.org/)  
[v3.vuejs.org](https://v3.vuejs.org/)  
[vue github](https://github.com/vuejs)

[intro to vue]: https://github.com/mouadeboussaid/aboutvue
[components]: https://github.com/MouadeBoussaid/aboutvue/tree/components
[exercise]: https://github.com/MouadeBoussaid/aboutvue/tree/components_exercise
[exercise solution]: https://github.com/MouadeBoussaid/aboutvue/tree/components_exercise_result
