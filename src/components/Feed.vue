<template>
    <ListView for="item in feed_items" @itemTap="click()" class="list">
        <v-template>
            <FeedItem title="Title" author="Author"/>
        </v-template>
    </ListView>
    
</template>

<script>
import FeedItem from './FeedItem';

export default {
    
    data(){
        return {
            post_title: "Post",
            poster: 'Name',
            feed_items: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
        }
    },
    components:{
        FeedItem
    },
    methods:{
       
        click(){
            confirm({
                title:"Go To Post?",
                message:"Going to watch debate",
                okButtonText: "Yes!",
                cancelButtonText: "Not Yet."
            }).then(result =>{
                console.log(result)
            });
        },
        genFeed(){
            var feed_items = [];
            var i;
            for(i=0; i<20;i++){
                var item = { title:"Post Title",poster:"Name",}
                feed_items.push(item)

            }

        }
    }
}
</script>

<style scoped>
    .words{
        color:black;
    }
    .feed-view{
        background-color: beige;
    }
</style>