# Coding challenge for Sr Software Engineer (Frontend)/Technical Lead (UI and Graphics)

## Purpose
Aim of these tests are to,

- evaluate your software engineering capability
- benchmark your technical experience and maturity
- understand how you design and implement your solution

## How you will be judged
You will be scored on,

- coding style, comments, and logging (20%)
- design patterns and algorithms (20%)
- solution design - structure and quality (20%)
- use of source control and documentation (20%)
- considerations for CI/CD/DevExp (10%)
- some basic unit/functional/E2E tests (10%)

## Instructions

1. Create a base VueJS app using [Vue CLI](https://cli.vuejs.org/guide/installation.html). 
2. For UI, you can use [Vue Bootstrap](https://bootstrap-vue.js.org/) and or [Vue Ant Design](https://vue.ant.design/docs/vue/introduce/)
3. In the root of the app, add a view that renders the geoJSON data provided in [this file](testBlob.json).
4. The root view has two main components:
- A Sidebar component that renders various filters populated based on the data attributes and associated values given in the geoJSON file. A filter can be a slider, an autocomplete, dropdown select, or switch.
- A Map display component that displays the Mapbox map and overlays geo-data points provided in the file on top of it. You can use [Vue-Mapbox wrapper](https://github.com/soal/vue-mapbox) or directly use [Mapbox GL JS library](https://github.com/mapbox/mapbox-gl-js).
- Create the binding between filter interactions and map display - so when a user interacts with the sidebar filter, the map gets updated with the matching condition.
5. Add your app as Github repo and send us the link for the code review. Add a `Readme.md` file in your repository with instructions to build the app locally.
6. Bonus point if you want to deploy your app to Netlify using their free accounts.

## Finally
Once you finished the test, either send us a pull request or URL for your Github repository.
