# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

Learn more about IDE Support for Vue in the [Vue Docs Scaling up Guide](https://vuejs.org/guide/scaling-up/tooling.html#ide-support).
## Organisation des composants

`App.vue` est le composant parent principal. Il affiche l’en-tête, la liste des recettes et le pied de page.

    App.vue
    ├── AppHeader.vue
    ├── RecipeList.vue
    │   └── RecipeCard.vue (une carte par recette)
    └── RecipeFooter.vue

`App.vue` contient le tableau `recipes` et le transmet à `RecipeList` avec la prop `recipes`. `RecipeList` parcourt ce tableau avec `v-for` et transmet chaque recette à une `RecipeCard` avec la prop `recipe`.