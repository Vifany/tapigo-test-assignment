<template>
  <div class="comment-entry">
    <p class="comment-text">{{ comment.text }}</p>
    <p class="comment-date">Date: {{ comment.date }}</p>
    
    <button v-if="renderSubcomment" @click="toggleCommentForm" class="btn btn-sm btn-secondary">Comment</button>

    <CommentForm v-if="showCommentForm && renderSubcomment" />

    <CommentEntry
      :renderSubcomment = false
      v-for="subcomment in comment.subComments"
      :key="subcomment.id"
      :comment="subcomment"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref} from 'vue';
import CommentForm from '~/components/CommentForm.vue';

export default defineComponent({
  props: {
    comment: Object,
    renderSubcomment:
      {
        type: Boolean, 
        default: true
      }
  },
  setup(props) {
    const showCommentForm = ref(false);

    const toggleCommentForm = () => {
      showCommentForm.value = !showCommentForm.value;
    };


    return {
      showCommentForm,
      toggleCommentForm,
    };
  },
});
</script>