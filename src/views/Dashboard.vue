<template>
  <div class="flex min-h-screen">
    <Sidebar />
    <div class="flex-1 bg-gray-100">
      <TopBar />
      <div class="p-6">
        <ProgressTracker />
        <div class="grid grid-cols-2 gap-6 mt-6">
          <CaloriesChart />
          <OverviewToday />
        </div>
        <div class="mt-6">
          <RecipesList />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Sidebar from '@/components/Sidebar.vue'
import TopBar from '@/components/TopBar.vue'
import ProgressTracker from '@/components/ProgressTracker.vue'
import CaloriesChart from '@/components/CaloriesChart.vue'
import OverviewToday from '@/components/OverviewToday.vue'
import RecipesList from '@/components/RecipesList.vue'
</script>
