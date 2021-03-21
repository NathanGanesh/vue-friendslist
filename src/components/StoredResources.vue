<template>
  <ul class="card-list">
    <div
      v-for="resourceItem in storedResourcesItems"
      :key="resourceItem"
      class="card"
    >
      <div class="details">
        <h4>{{ resourceItem.title }}</h4>
        <h5>{{ resourceItem.description }}</h5>
        <a :href="resourceItem.link">View Resource</a>
      </div>
      <div class="delete">
        <button :value="resourceItem.title">Delete</button>
      </div>
    </div>
  </ul>
</template>
<style>
.card-list {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 0rem auto;
  width: 650px;
}
ul {
  list-style-type: disc;
  margin-block-start: 0em;
  margin-block-end: 0em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 0px;
}
.card {
  box-shadow: 0 2px 8px rgb(0 0 0 / 26%);
  border-radius: 12px;
  margin: 10px;
  display: flex;
  justify-content: space-between;
}
.details {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  text-align: start;
  margin: 5px 25px;
  /* padding: 16px 0px; */
}
.delete {
  margin: 25px 25px;
}
</style>
<script>
export default {
  props: ['storedResourcesItems'],
  data() {}
  // phoneNumber: {
  //   type: String,
  //   required: false
  // }
};
</script>
