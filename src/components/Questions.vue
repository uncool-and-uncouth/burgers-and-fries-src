<template>
    <div class="questions">
        <dies @partyDies="doesDie = $event"></dies>
        <ends v-if="doesDie !== null && !doesDie" @partyEnds="doesEnd = $event"></ends>
        <iframe 
            class="video"
            width="560" 
            height="315" 
            src="https://www.youtube.com/embed/AezjzBTAbO0?autoplay=1" 
            frameborder="0" 
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen
            v-if="!doesDie && doesDie !== null && !doesEnd && doesEnd !== null"
        >
        </iframe>
    </div>
</template>
<script>
import Dies from './Dies'
import Ends from './Ends'
export default {
  name: 'app',
  components: {
    Dies,
    Ends
  },
  data () {
    return {
      doesDie: null,
      doesEnd: null
    }
  }
}
</script>
<style scoped>
    .video {
        margin: 20px;
    }
</style>


