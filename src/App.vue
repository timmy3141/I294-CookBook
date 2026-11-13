<script setup>
import AppHeader from './components/AppHeader.vue'
import RecipeList from './components/RecipeList.vue'
import RecipeFooter from './components/RecipeFooter.vue'

// Les données de nos recettes
const recipes = [
  {
    id: 1,
    name: 'Spaghetti au steak',
    description: 'Délicieuses pâtes à la sauce de steak.',
    time: 20,
    difficulty: 'Facile',
    emoji: '🍝',
    persons: 2
  },
  {
    id: 2,
    name: 'Pizza au Steak',
    description: 'Pizza maison au steak.',
    time: 35,
    difficulty: 'Moyen',
    emoji: '🍕',
    persons: 1
  },
  {
    id: 3,
    name: 'Gâteau au steak',
    description: 'Gâteau au steak fait maison.',
    time: 45,
    difficulty: 'Facile',
    emoji: '🍰',
    persons: 4
  },
  {
    id: 4,
    name: 'Steak',
    description: 'Steak de boeuf fraichement abattu',
    time: 50,
    difficulty: 'Hardcore',
    emoji: '🥩',
    persons: "6 ou 7"
  },
  {
    id: 5,
    name: 'Glace au steak',
    description: 'Glace saveur steak',
    time: 50,
    difficulty: 'Difficile',
    emoji: '🍨',
    persons: 25
  },
  {
    id: 6,
    name: 'Salade de steak',
    description: 'Tranche de steak finement coupées en salade',
    time: 50,
    difficulty: 'Paisible',
    emoji: '🥗',
    persons: 116
  }
]
</script>

<template>
  <div class="app">
    <!-- Composant enfant : en-tête -->
    <AppHeader />

    <main>
      <section class="hero">
        <h1>Bienvenue dans ma cuisine !</h1>
        <p>Découvrez des recettes simples et délicieuses.</p>
      </section>

      <!-- Composant enfant : liste des recettes -->
      <RecipeList :recipes="recipes" />
    </main>
    <RecipeFooter />
  </div>
</template>

<style scoped>
.app {
  min-height: 100vh;
}

.hero {
  background: #e8f1ec;
  padding: 50px 30px;
  text-align: center;
}

.hero h1 {
  color: #173d35;
  font-size: 32px;
}

.hero p {
  color: #526b60;
}

footer {
  background: #173d35;
  color: white;
  text-align: center;
  padding: 20px;
  margin-top: 40px;
  font-size: 13px;
}
</style>