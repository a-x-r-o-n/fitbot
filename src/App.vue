<template>
  <div class="flex flex-col lg:flex-row min-h-screen font-sans">
    <Sidebar :navBar="navBar" @changeNav="navBar = $event" />
    <div class="flex-1 bg-gray-100 dark:bg-[#0f1a24] text-white">
      <TopBar :navBar="navBar" />
      <main v-if="navBar === 0" class="p-4 sm:p-6 md:p-8 lg:p-10 space-y-6 max-w-screen-2xl mx-auto">
        <ProgressTracker :weight="weight" :height="height" :bmi="getBmi()"/>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <CaloriesChart />
          <OverviewToday />
        </div>
        <RecipesList />
      </main>

      <main v-else-if="navBar === 1" class="p-4 sm:p-6 md:p-8 lg:p-10 space-y-6 max-w-screen-2xl mx-auto">
        <UserInputForm />
      </main>


    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      navBar: 0,
      weight: 78.95,
      height: 170.00
    }
  },
  methods: {
    getBmi(){
      return this.weight && this.height? (this.weight / ((this.height/100) * (this.height/100))).toFixed(2) : "-"
    }
  }
}

</script>
<script setup>
import Sidebar from './components/Sidebar.vue'
import TopBar from './components/TopBar.vue'
import ProgressTracker from './components/ProgressTracker.vue'
import UserInputForm from './components/UserInputForm.vue'
import CaloriesChart from './components/CaloriesChart.vue'
import OverviewToday from './components/OverviewToday.vue'
import RecipesList from './components/RecipesList.vue'
</script>