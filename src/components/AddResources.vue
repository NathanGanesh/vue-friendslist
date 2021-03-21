<template>
  <div>
    <form class="form-box">
      <label for="title">Title</label>
      <input type="text" id="title" name="title" />

      <label for="description">Description</label>
      <input type="textarea" id="description" name="description" />

      <label for="link">Link </label>
      <input type="text" id="link" name="link" />
      <button type="submit" id="btn">Add Resource</button>
    </form>
  </div>
</template>

<style>
.form-box {
  width: 650px;
  text-align: start;
  box-shadow: 0 2px 8px rgb(0 0 0 / 26%);
  margin: 0 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;

  border-radius: 12px;
}
.form-box label {
  font-weight: 800;
  margin-bottom: 50px;
}
input {
  width: 650px;
  margin: auto;
}
#link {
  margin-bottom: 20px;
}
#btn {
  width: 125px;
  height: 35px;
}

#description {
  height: 170px;
}
</style>
<script></script>
