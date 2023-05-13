<template>
  <div>
    <div>
      <h3>List of users</h3>
    </div>
    <div>
      <PostItem v-for="post in posts" :post="post" v-bind:key="post.id" />
    </div>
  </div>
</template>

<script>
import PostItem from "@/components/PostItem";

export default {
  components: {
    PostItem,
  },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  list-style-type: none;
  text-decoration: none;
  box-sizing: border-box;
  font-family: sans-serif;
}

.post {
  padding: 15px;
  border: 2px solid teal;
  margin: 10px;
}

.input,
.btn {
  display: block;
  padding: 15px;
  width: 90%;
  margin: 10px;
  border: 2px solid teal;
}
</style>