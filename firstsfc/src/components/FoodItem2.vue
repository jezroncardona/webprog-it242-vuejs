<template>
  <div class="pearto">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Pears',
      message: 'I like pears. Peartos!'
    }
  }
};
</script>

<style>
  .pearto {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>