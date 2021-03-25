<template>
    <Page class="main-screen">
      <ActionBar title="Debate"/>
       <TabView>
          <TabViewItem title="Feed">
             <Feed />
          </TabViewItem>
          <TabViewItem title="Profile">
            <Label text="Profile" class="title"/>
             
          </TabViewItem>
       </TabView>
    </Page>
</template>

<script >
  
  import Feed from './Feed'
  import FeedItem from './FeedItem';
  export default {
    data() {

      return {
        currentComponent: 'Feed',
        componentsArray: ['Feed']
      }
    },
    components: {
       Feed, FeedItem
    }
  }
</script>

<style scoped>
  
   .main-screen{
    background-color: rgb(236, 230, 138);
   }
  .nav-button{
    background-color: rgb(133, 111, 92);
    color:whitesmoke;
  }
   .title{
    color:black;
    text-align: center;
    font-size:45px;
    
   }
</style>
