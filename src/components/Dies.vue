<template>
    <div class="dies">
        <p>Does the party die?</p>
        <button @click="doesPartyDie(true)" :disabled="clicked">Yes</button>
        <button @click="doesPartyDie(false)" :disabled="clicked">No</button>
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
        doesPartyDie (bool) {
            this.$emit('partyDies', bool)
            this.clicked = true 
        }
    }
}
</script>
<style scoped>
    .dies {
        margin: 10px;
    }
</style>


