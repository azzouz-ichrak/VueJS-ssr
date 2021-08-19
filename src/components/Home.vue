<template>
  <div class="content">
     -- {{ count }} --<br />
    <button v-on:click.prevent="increment">+</button>
    <button v-on:click.prevent="decrement">-</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  data: () => {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.content {
  padding: 5%;
  font-weight: bold;
  text-align: center;
}
</style>
