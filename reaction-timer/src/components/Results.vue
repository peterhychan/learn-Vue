<template>
  <p>Reaction Time: {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
  props: ["score"],
  data(){
    return{
      rank: null
    }
  },
  mounted(){
    if(this.score < 250){
      this.rank = "S Class"
    }else if(this.score <400){
      this.rank = "A Class"
    }else{
      this.rank = "B Class"
    }
  }
}
</script>

<style>
.rank{
  font-size: 1.5em;
  color: #00ffaa;
  font-weight: bold;
}
</style>