<template>
  <ul>
    <!-- bind all props and provide values to all props in learning resources -->
    <learning-resources
      v-for="res in storedResources"
      :key="res.id"
      :title="res.title"
      :description="res.describtion"
      :link="res.link"
    >
    </learning-resources>
  </ul>
</template>
<script>
import LearningResources from './components/learning-resources/LearningResource.vue';
export default {
  components: {
    LearningResources
  },

  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          describtion: 'The Official Vue js documentation',
          link: 'https://vuejs.org'
        },
        {
          id: 'Google',
          title: 'Google',
          describtion: 'Learn to google',
          link: 'https://google.org'
        }
      ]
    };
  }
};
</script>
