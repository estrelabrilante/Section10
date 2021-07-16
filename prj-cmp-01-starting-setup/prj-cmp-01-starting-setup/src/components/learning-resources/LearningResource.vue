<template>
  <li>
    <div>
      <header>
        <!-- Title -->
        <h3>{{ title }}</h3>
        <button>
          Delete
        </button>
      </header>
    </div>
    <!-- Description -->
    <p>{{ description }}</p>
    <nav>
      <!-- Link -->
      <a v-bind:href="link">View Resource</a>
    </nav>
  </li>
</template>
<script>
export default {
  // with props : gets external data by making components reusable and configurable
  props: ['title', 'description', 'link']
};
</script>
