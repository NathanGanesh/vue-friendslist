<template>
  <div>
    <button @click="setSelectedComponent('stored-resources')">
      Stored Resources
    </button>
    <button @click="setSelectedComponent('add-resources')">
      Add Resources
    </button>
    <keep-alive>
      <component :is="selectedComponent"></component>
    </keep-alive>
  </div>
</template>

<script>
export default {};
</script>
