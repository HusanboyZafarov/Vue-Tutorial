<template>
  <div>
    <post-form @create="createPost"></post-form>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  components: {
    PostForm,
    PostList,
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "Vue js",
          description: "I'm learning it",
        },
        {
          id: 2,
          title: "Hyper Text markup language",
          description: "I'm learned it",
        },
        {
          id: 3,
          title: "css 3",
          description: "cool lang but not lang",
        },
      ],
      title: "",
      body: "",
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
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
button {
  display: block;
  padding: 15px;
  width: 90%;
  margin: 10px;
  border: 2px solid teal;
}
</style>