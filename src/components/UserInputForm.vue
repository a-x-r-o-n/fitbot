<template>
  <div class="bg-white dark:bg-gray-900 p-4 md:p-6 rounded-xl shadow-lg w-full">
    <h2 class="text-lg md:text-xl font-semibold mb-4">Track Your Daily Input</h2>
    <form @submit.prevent="handleSubmit" class="space-y-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
        <!-- <div>
          <label class="block text-sm font-medium mb-1">Date</label>
          <input v-model="date" type="date" class="w-full p-2 rounded border dark:bg-gray-800 dark:text-white" required />
        </div> -->
        <div>
          <label class="block text-sm font-medium mb-1">Weight (kg)</label>
          <input v-model="weight" type="number" step="0.1" class="w-full p-2 rounded border dark:bg-gray-800 dark:text-white" required />
        </div>
        <div>
          <label class="block text-sm font-medium mb-1">Calories Consumed</label>
          <input v-model="calories" type="number" class="w-full p-2 rounded border dark:bg-gray-800 dark:text-white" required />
        </div>
        <div>
          <label class="block text-sm font-medium mb-1">Protein (g)</label>
          <input v-model="protein" type="number" step="0.1" class="w-full p-2 rounded border dark:bg-gray-800 dark:text-white" required />
        </div>
      </div>
      <button type="submit" class="mt-4 bg-yellow-400 hover:bg-yellow-300 text-black px-4 py-2 rounded-lg font-semibold">Submit</button>
    </form>
    <div v-if="submitted" class="mt-4 text-sm text-green-400">
      Data submitted for {{ date }}: Weight - {{ weight }}kg, Calories - {{ calories }}, Protein - {{ protein }}g
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const date = ref('')
const weight = ref('')
const calories = ref('')
const protein = ref('')
const submitted = ref(false)

function handleSubmit() {
  submitted.value = true
  console.log({ date: date.value, weight: weight.value, calories: calories.value, protein: protein.value })
}
</script>