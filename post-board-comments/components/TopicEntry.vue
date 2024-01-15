<template>
  <div class="container-sm mt-4">
    <div class="card">
      <div class="card-body">
        <h2 class="card-title">{{ topic.header }}</h2>
        <img v-if="!expanded" :src="topic.image" class="img-fluid" alt="Topic Image" />

        <div v-if="!expanded">
          <p class="card-text">{{ topic.description.slice(0, 20) }}...</p>
          <button @click="toggleExpanded" class="btn btn-primary">Expand</button>
        </div>

        <div v-if="expanded" class="mt-3">
          <img :src="topic.image" class="img-fluid" alt="Large Topic Image" />
          <p class="card-text">Creation Date: {{ topic.creationDate }}</p>
          <p class="card-text">{{ topic.description }}</p>
          <button @click="toggleExpanded" class="btn btn-primary">Collapse</button>

          <CommentEntry
            v-for="comment in topic.comments"
            :key="comment.id"
            :comment="comment"
          />

          <CommentForm />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import CommentEntry from '~/components/CommentEntry.vue';
import CommentForm from '~/components/CommentForm.vue';

export default defineComponent({
  components: {
    CommentEntry,
    CommentForm,
  },
  props: {
    topic: Object,
  },
  setup(props) {
    const expanded = ref(false);

    const toggleExpanded = () => {
      expanded.value = !expanded.value;
    };

    return {
      expanded,
      toggleExpanded,
    };
  },
});
</script>
