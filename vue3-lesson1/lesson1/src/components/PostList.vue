<template>
    <div>
        <div class="post" v-for="post in posts">
            <div><b>Name:</b> {{ post.title }}</div>
            <div><b>Description:</b> {{ post.body }} </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true
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