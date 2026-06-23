<script setup>
import logo from '@/assets/logo.svg'
</script>

  
<template>
<!-- Navbar -->
 <nav class="bg-white shadow-md">
  <div class="max-w-7xl mx-auto px-4">
    <div class="flex justify-between items-center h-16">
      
      <!-- Logo -->
      <div class="flex items-center">
       <img class="h-10 w-auto" :src="logo" alt="Vue Jobs">
      </div>

      <!-- Navigation Links -->
      <div class="flex space-x-6">
        <a href="#" class="text-gray-700 hover:text-blue-600">
          Home
        </a>
        <a href="#" class="text-gray-700 hover:text-blue-600">
          About
        </a>
        <a href="#" class="text-gray-700 hover:text-blue-600">
          Services
        </a>
        <a href="#" class="text-gray-700 hover:text-blue-600">
          Contact
        </a>
      </div>

    </div>
  </div>
</nav>


</template>


<style>
</style>