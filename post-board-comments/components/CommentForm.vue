<template>
  <div class="container mt-4">
    <div class="card">
      <div class="card-body">
        <form class="comment-form">
          <div class="mb-3">
            <textarea class="form-control" v-model="commentText" placeholder="Type your comment"></textarea>
          </div>
          <button class="btn btn-primary btn-sm" @click="sendComment">Send</button>
        </form>
      </div>
    </div>
  </div>
</template>
  
  <script lang="ts">
    import {defineComponent, ref } from 'vue';

    export default defineComponent({
      setup() {
        const commentText = ref('');

        const sendComment = () => {
          // Handle comment submission logic here
          console.log('Comment sent:', commentText.value);
          // Clear the textarea after sending the comment
          commentText.value = '';
        };

        return {
          commentText,
          sendComment,
        };
      },
    });
  </script>
  
