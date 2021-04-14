<template>
    <StackLayout class="post">
        <Label class="title h1" :text="title"/>
        <Label class="title h2" :text="author"/>
        <VideoPlayer ref="player" src="https://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4" autoplay="true" height="300"></VideoPlayer>
    </StackLayout>
</template>

<script>

export default {
    data(){
        return{
            videoContent: "<video width=\"300\" height=\"200\" controls><source src= \"src/doit_clipped.mp4\" type=\"video/mp4\"/></video>",
            video: "doit_clipped.mp4"
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
       
        color:rgb(0, 0, 0);
    }
    .user{
        font-size: 20px;
        color:rgb(74, 72, 228);
    }
    .post{
        background-color: cornsilk;
    }
</style>