<template>
  <div class="global-container">
    <TopicList />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import TopicList from '~/components/TopicList.vue';
import 'bootstrap/dist/css/bootstrap.css'

export default defineComponent({
  components: {
    TopicList,
  },
});
</script>