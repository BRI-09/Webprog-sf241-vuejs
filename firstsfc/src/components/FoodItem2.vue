<template>
  <div class="pinapple"></div>
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Pineaple and Milk',
      message: 'Shake shake shake'
    }
  }
};
</script>

<style>
    .pineaplle {
    border: dashed rgb(12, 0, 0) 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: rgb(223, 241, 116);
  }
</style>