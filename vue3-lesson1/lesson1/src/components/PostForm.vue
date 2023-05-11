<template>
    <div>
        <form @submit.prevent>
            <h1>Creating post</h1>
            <input v-model="post.title" class="input" type="text" placeholder="title">
            <input v-model="post.body" class="input" type="text" placeholder="description">
            <button @click="createPost">create</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            post: {
                title: '',
                body: ''
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now()
            this.$emit('create', this.post)
            this.post = {
                title: '',
                body: ''
            }
        }
    }
}
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