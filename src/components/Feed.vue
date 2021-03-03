<template>
   <ListView for="item in items" @itemTap="click">
            <v-template>
                <FeedItem :title="post_title" :author="poster"/>
            </v-template>
    </ListView>
    
</template>

<script>
import FeedItem from './FeedItem';
import posts from '../data/posts.json';
import users from '../data/users.json';
export default {
    
    data(){
        return {
            post_title: this.getTitle(),
            poster: this.getName(),
            items: this.gatherFeed()
        }
    },
    components:{
        FeedItem
    },
    methods:{
        getTitle(){
            const post_id = Math.floor(Math.random() * 100) - 1
            
            return posts[post_id.toString()]["title"]
        },
        getName(){
            const user_id = Math.floor(Math.random() * 49) - 1
            return users[user_id.toString()]["name"]
        },
        gatherFeed(){
            var feeditems = []
            var titles = []
            var i;
            for(i =0;i<20;i++){
                const post = { title:this.getTitle(), poster:this.getName() }
                feeditems.push(post)
                titles.push(this.getTitle())
            }
            
            return feeditems;
        },
        click(){
            confirm({
                title:"Go To Post?",
                message:"Going to watch debate",
                okButtonText: "Yes!",
                cancelButtonText: "Not Yet."
            }).then(result =>{
                console.log(result)
            });
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