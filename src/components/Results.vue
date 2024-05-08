<template>
    <p>Reaction time - {{ score }}</p>
    <p class="rank">Your rank: {{ rank }}</p>
</template>


<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Max Verstappen'
        } else if (this.score < 400) {
            this.rank = 'Medium'
        } else {
            this.rank = 'Zzz'
        }
    }

}

</script>


<style>
.rank {
    font-size: 1.4em;
    color: #5018a3;
    font-weight: bold;
}

</style>