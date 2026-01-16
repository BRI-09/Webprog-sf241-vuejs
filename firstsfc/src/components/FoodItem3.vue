<template>
  <div class="banana">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Banana and Strawberry',
      message: 'Shake shake shake'
    }
  }
};
</script>

<style>
    .banana {
    border: dashed rgb(12, 0, 0) 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: rgb(225, 237, 83);
  }
</style>