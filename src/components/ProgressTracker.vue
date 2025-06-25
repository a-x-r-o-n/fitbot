<script>
export default {
  name: 'ProgressTracker',
  props: {"weight": Number, "height": Number, "bmi": Number},
}
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-6 gap-4 text-white">
    <div class="HvrBtn-1 bg-yellow-400 p-4 md:p-6 rounded-xl text-black shadow-lg">
      <div class="text-sm md:text-base font-medium">Calories</div>
      <div class="text-2xl md:text-3xl font-bold">6.778 Kcal</div>
    </div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Proteins Consumed<br><span class="text-lg md:text-xl font-semibold">155 ml</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Carbs Consumed<br><span class="text-lg md:text-xl font-semibold">290 ml</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Weight<br><span class="text-lg md:text-xl font-semibold">{{ weight? weight : "-" }} Kg</span></div>
    <div class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">Height<br><span class="text-lg md:text-xl font-semibold">{{ height? height : "-" }} Cm</span></div>
    <div :class="bmi < 18.5 ? 'text-blue-600' :bmi <= 25 ? 'text-green-600' :bmi <= 30 ? 'text-yellow-600' : 'bg-red-600 text-black' " class="HvrBtn bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg">BMI<br><span class="text-lg md:text-xl font-semibold">{{bmi}}</span></div>
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