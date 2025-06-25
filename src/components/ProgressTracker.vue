<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-6 gap-4 text-white">
    <div class="HvrBtn-1 bg-yellow-400 p-4 md:p-6 rounded-xl text-black shadow-lg">
      <div class="text-sm md:text-base font-medium">Avg Calories</div>
      <div class="text-2xl md:text-3xl font-bold">6.778 Kcal</div>
    </div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Avg Proteins<br><span class="text-lg md:text-xl font-semibold">155 ml</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Avg Carbs<br><span class="text-lg md:text-xl font-semibold">290 ml</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Weight<br><span class="text-lg md:text-xl font-semibold">78 Kg</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Height<br><span class="text-lg md:text-xl font-semibold">170 Cm</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">BMI<br><span class="text-lg md:text-xl font-semibold">27</span></div>
  </div>
</template>

<style scoped>

.HvrBtn{
    transition: 0.3s;
}
.HvrBtn:hover{
    background-color: #FACC15;
    color: black;
}
.HvrBtn-1:hover{
    color: white;
}
</style>