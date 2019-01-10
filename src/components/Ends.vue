<template>
    <div class="ends">
        <p>Does the party end?</p>
        <button @click="doesPartyEnd(true)" :disabled="clicked">Yes</button>
        <button @click="doesPartyEnd(false)" :disabled="clicked">No</button>
    </div>
</template>
<script>
export default {
    name: 'dies',
    data () {
        return {
            clicked: false
        }
    },
    methods: {
        doesPartyEnd (bool) {
            this.$emit('partyEnds', bool)
            this.clicked = true 
        }
    }
}
</script>
<style scoped>
    .ends {
        margin: "10px"
    }
</style>

