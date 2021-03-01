<template>
    <ScrollView orientation="vertical" class="feed-view">
        <StackLayout orientation="vertical">
            <FeedItem/>
        </StackLayout>
    </ScrollView>
</template>

<script>
import FeedItem from './FeedItem'
export default {
    
    data(){
        return {
            title: "Feed"
        }
    },
    components:{
        FeedItem
    }
}
</script>

<style scoped>
    .feed-view{
        background-color: beige;
    }
</style>