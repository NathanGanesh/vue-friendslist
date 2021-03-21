<template>
  <div v-if="selectedComponent !== undefined">
    <div class="selected-component">
      <button
        v-if="selectedComponent"
        @click="setSelectedComponent('stored-resources')"
        v-bind:class="[{ active: selectedComponent === 'stored-resources' }]"
      >
        Stored Resources
      </button>
      <button
        @click="setSelectedComponent('add-resources')"
        v-bind:class="[{ active: selectedComponent === 'add-resources' }]"
      >
        Add Resources
      </button>
    </div>
    <keep-alive>
      <component
        :is="selectedComponent"
        v-bind="currentProps"
        class="tab"
      ></component>
    </keep-alive>
  </div>
</template>

<script>
import AddResources from '@/components/AddResources';
import StoredResources from '@/components/StoredResources';

export default {
  components: {
    AddResources,
    StoredResources
  },
  data() {
    return {
      selectedComponent: 'stored-resources',

      storedResourcesItems: [
        {
          title: 'Official guide',
          description: 'The official vue.js documentation',
          link:
            'http://www.westernspring.co.uk/the-coudenhove-kalergi-plan-the-genocide-of-the-peoples-of-europe/'
        },
        {
          title: 'Official guide',
          description: 'The official vue.js documentation',
          link:
            'http://www.westernspring.co.uk/the-coudenhove-kalergi-plan-the-genocide-of-the-peoples-of-europe/'
        }
      ]
    };
  },
  methods: {
    setSelectedComponent(cmp) {
      this.selectedComponent = cmp;
    },
    deleteItem(itemName) {
      this.storedResourcesItems.filter(item => {
        itemName !== item.title;
      });
    },
    addNewItem(data) {
      console.log(data);
    }
  },
  computed: {
    currentProps: function() {
      if (this.selectedComponent === 'stored-resources') {
        console.log(this.selectedComponent);
        return { storedResourcesItems: this.storedResourcesItems };
      } else {
        console.log(this.selectedComponent);
        return { addNewItem: this.addNewItem };
      }
    }
  }
};
</script>
<style scoped>
.selected-component {
  margin: 2rem auto;
  width: 650px;
  padding: 20px;
  box-shadow: 0 2px 8px rgb(0 0 0 / 26%);
  border-radius: 12px;

  display: flex;
  flex-direction: row;
}
button {
  height: 45px;
  width: 125px;
  border: 0px;
}
.active {
  /* background */
  background: rgb(247, 58, 247);
}
button:hover {
  cursor: pointer;
  background-color: rgb(43, 3, 43);
}
</style>
