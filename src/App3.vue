<template>
  <h3>{{ name }}</h3>
  <h3>Status: {{ status }}</h3>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else="status">User is neither active or pending</p>

  <h3>
    <ul>
      <li v-for="task in tasks" :key="task">
        {{ task }}
      </li>
    </ul>
    <a v-bind:href="link">Click for google</a>
    <a :href="link">Using this link without v-bind, but just shorter way</a>
</h3>
<br />
<button v-on:click="toggleStatus">Change status</button>
<br />
<button @click="toggleStatus">Change status (another way)</button>
</template>

<style scoped>
h1 {
  color: blue;
}
</style>

<script>
export default {
  data() {
    return {
      name: "John",
      status: 'dd',
      tasks: ["task one", "task two"],
      link: "https://google.com"
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') {
        this.status = 'pending';
      } else if (this.status === 'pending') {
        this.status = 'inactive';
      } else {
        this.status = 'active';
      }
    }
  }
}
</script>