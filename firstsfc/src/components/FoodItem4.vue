<template>
  <div class="blueberry">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Blueberry',
      message: 'Coming Soon'
    }
  }
};
</script>

<style>
    .blueberry {
    border: dashed rgb(12, 0, 0) 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: rgb(31, 101, 206);
  }
</style>