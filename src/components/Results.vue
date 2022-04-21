<template>
  <p>Reaction Time - {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
props: ['score'],
data(){
    return {
        rank: null
    }
},
mounted(){
    if(this.score < 380){
        this.rank = 'Fast Response'
    }else if(this.score < 400){
        this.rank = 'Slow Response'
    }else{
        this.rank = 'Very Slow Response'
    }
}
}
</script>

<style>
    .rank{
        font-size: 1.4rem;
        color: #0faf87;
        font-weight: bold;
    }
</style>