<template>
  <div>
    <form @submit.prevent>
      <h1>Creating post</h1>
      <my-input v-model="post.title" type="text" placeholder="title" />
      <my-input v-model="post.body" type="text" placeholder="description" />
      <MyButton class="btn" @click="createPost">create</MyButton>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
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
  display: inline-block;
  padding: 15px;
  margin: 10px;
  border: 2px solid teal;
}
</style>