<template>
  <div class="flex flex-col lg:flex-row min-h-screen font-sans">
    <Sidebar />
    <div class="flex-1 bg-gray-100 dark:bg-[#0f1a24] text-white">
      <TopBar />
      <main class="p-4 sm:p-6 md:p-8 lg:p-10 space-y-6 max-w-screen-2xl mx-auto">
        <ProgressTracker />
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <CaloriesChart />
          <OverviewToday />
        </div>
        <RecipesList />
      </main>
    </div>
  </div>
</template>

<script setup>
import Sidebar from './components/Sidebar.vue'
import TopBar from './components/TopBar.vue'
import ProgressTracker from './components/ProgressTracker.vue'
import CaloriesChart from './components/CaloriesChart.vue'
import OverviewToday from './components/OverviewToday.vue'
import RecipesList from './components/RecipesList.vue'
</script>
