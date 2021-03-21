<template>
  <div>
    <the-header></the-header>
    <SelectedResourcesVue></SelectedResourcesVue>
  </div>
</template>
<style>
* {
  box-sizing: border-box;
}
html {
  font-family: sans-serif;
}
body {
  margin: 0;
}
</style>

<script>
import TheHeader from '@/components/layout/TheHeader';
import SelectedResourcesVue from './components/SelectedResources.vue';
export default {
  components: {
    TheHeader,
    SelectedResourcesVue
  },
  data() {
    return {
      selectedComponent: 'stored-resources'
    };
  },
  methods: {
    setSelectedComponent(cmp) {
      console.log('hit');
      this.selectedComponent = cmp;
    }
  }
};
</script>
