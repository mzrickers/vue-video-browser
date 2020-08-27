<template>
    <ul class="list-group">
        <VideoListItem 
            v-for="video in videoArray" 
            :video="video"
            :key="video.etag"
            @videoSelect="onVideoSelect2"
        >
        </VideoListItem>
    </ul>
    
</template>

<script>
import VideoListItem from './VideoListItem';

export default {
    name: 'VideoList',
     components: {
        VideoListItem
    },
    props: ['videoArray'],
    methods: {
        onVideoSelect2(video) {
            this.$emit('videoSelect', video)
        }
    }
}
</script>

<style scoped>

</style>