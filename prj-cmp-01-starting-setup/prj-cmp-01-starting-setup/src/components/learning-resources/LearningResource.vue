<template>
  <li>
    <base-card>
      <header>
        <!-- Title -->
        <h3>{{ title }}</h3>
        <button>
          Delete
        </button>
      </header>

      <!-- Description -->
      <p>{{ description }}</p>
      <nav>
        <!-- Link -->
        <a v-bind:href="link">View Resource</a>
      </nav>
    </base-card>
  </li>
</template>
<script>
export default {
  // with props : gets external data by making components reusable and configurable
  props: ['title', 'description', 'link']
};
</script>
<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>
