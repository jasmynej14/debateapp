<template>
    <Page class="main-screen">
    
       <AbsoluteLayout>
          <Label class="title" left="40" top="25" text="Make Your Point"/>
          <component
	          v-for="component in componentsArray"
	          v-show="component === currentComponent"
	          :is="component"
            :key="component"
	          left="10"
            top="100"
            />
          <Button class="nav-button" @tap="currentComponent= 'Feed'" left="10" top="700" text="Feed"/>
          <Button class="nav-button" @tap="currentComponent= 'Profile'" left="100" top="700" text="Profile"/>
          
       </AbsoluteLayout>
    </Page>
</template>

<script >
  import Feed from './Feed'
  import Profile from './Profile'
  export default {
    data() {

      return {
        currentComponent: 'Feed',
        componentsArray: ['Feed','Profile']
      }
    },
    components: {
       Feed,Profile
    }
  }
</script>

<style scoped>
  
   .main-screen{
    background-color: aliceblue;
   }
  .nav-button{
    background-color: rgb(115, 133, 92);
    color:whitesmoke;
  }
   .title{
    color:black;
    font-size:45px;
    
   }
</style>
