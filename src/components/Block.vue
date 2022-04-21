<template>
  <div class="block" v-if='showBlock'>
      Click Me
  </div>
</template>

<script>
export default {
props: ['delay'],
data(){
    return{
        showBlock: false
    }
},
mounted(){
    console.log('component mounted')
    setTimeout(() => {
        this.showBlock = true
        console.log(this.delay)
    }, this.delay)
},
// updated(){
//     console.log('component updated')
// },
// unmounted(){
//     console.log('component unmounted')
// }

}
</script>

<style>
.block{
    width: 50%;
    background: salmon;
    color: white;
    margin: 40px auto;
   padding: 150px 0;
}
</style>