<template>
  <div>
    <div class="post">
      <div><b>Name:</b> {{ post.title }}</div>
      <div><b>Description:</b> {{ post.description }}</div>
      <div class="post__btns">
        <MyButton class="btn">Delete</MyButton>
      </div>
    </div>
  </div>
</template>

<script>
import MyButton from "./UI/MyButton.vue";
export default {
  components: { MyButton },
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
</style>