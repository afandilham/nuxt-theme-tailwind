<template>
  <div class="h-screen bg-gray-300 dark:bg-gray-800 transition-all grid place-items-center">
    <div class="flex gap-4 items-center justify-center">
      <button class="font-semibold text-sm border-none outline-none px-6 py-2 rounded-sm bg-white" @click="changeTheme('light')">Light</button>
      <button class="font-semibold text-sm border-none outline-none px-6 py-2 rounded-sm bg-gray-600 text-white" @click="changeTheme('dark')">Dark</button>
    </div>
  </div>
</template>

<script setup>
const colorMode = useColorMode();

const changeTheme = (color) => {
  colorMode.preference = color;
  console.log(colorMode.preference);
};
</script>
