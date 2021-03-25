<template>
    <StackLayout class="post">
        <Label class="title" :text="title"/>
        <Label class="user" :text="author"/>
        <Image src="https://image.shutterstock.com/image-vector/young-politician-male-female-speakers-260nw-1551587897.jpg" stretch="none"/>
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
        color:rgb(231, 107, 107);
    }
    .user{
        font-size: 20px;
        color:rgb(74, 72, 228);
    }
    .post{
        background-color: cornsilk;
    }
</style>