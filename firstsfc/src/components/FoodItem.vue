<template>
  <div class="papaya">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Papaya and Pineaple',
      message: 'Shake shake shake'
    }
  }
};
</script>

<style>
    .papaya {
    border: dashed rgb(12, 0, 0) 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: rgb(240, 152, 58);
  }
</style>