<template>
   <GridLayout rows="auto,auto,auto,auto,auto,auto" columns="auto,auto,auto" horizontalAlignment="center">
       <Label text="[profile image]" row="0" col="1" class="h1"/>
       <Label text="[username]" row="1" col="1" class="h1"/>
       <StackLayout class="hr m-10" row="2" colSpan="3"></StackLayout>
       <Label text="[# Following]" row="3" col="0"/>
       <Label text="[# Followers]" row="3" col="1"/>
       <Label text="[#Likes]" row="3" col="2"/>
      
   </GridLayout>
</template>

<script>
export default {
    data(){
        return{

        }
    }
}
</script>

<style scoped>
    .filler{
        font-size: 45px;
        color:black;
    }
</style>