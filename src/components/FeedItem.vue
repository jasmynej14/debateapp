<template>
    <StackLayout class="post">
        <Label class="title" :text="title"/>
        <Label class="user" :text="author"/>
      
    </StackLayout>
</template>

<script>
 import posts from '../data/posts.json'
 import users from '../data/users.json'
export default {
    data(){
        return{
        }
       
    },

    props:{
        title: String,
        author: String
    },
    methods:{
        getTitle(){
            const id = Math.floor(Math.random() * 100) - 1
            return posts[id]["title"]
        },
        getName(){
            const id = Math.floor(Math.random() * 50) - 1
            return users[id]["name"]
        }
    }
}
</script>

<style scoped>
    .title{
        font-size: 35px;
        color:black;
    }
    .user{
        font-size: 20px;
        color:black;
    }
    .post{
        background-color: cornsilk;
    }
</style>