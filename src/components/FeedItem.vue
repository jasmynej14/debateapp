<template>
    <StackLayout class="post">
        <Label class="title" :text="title"/>
        <Label class="user" :text="author"/>
        
    </StackLayout>
</template>

<script>

export default {
    data(){
        return{
            videoContent: "<video width=\"300\" height=\"200\" controls><source src= \"src/doit_clipped.mp4\" type=\"video/mp4\"/></video>"
        }
       
    },

    props:{
        title: String,
        author: String
    },
    methods:{
        
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