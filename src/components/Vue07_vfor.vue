<template>
  <h1>v-for</h1>

     <span v-for="item2 in 3" :key="item2">
        <span class ="s" v-for="item in 9" :key="item"><br>
            <span v-for="item1 in 3" :key="item1">&nbsp;&nbsp;
               <span v-if="item1>3">
            {{(item1+1)+3}}X{{item}}={{(item1+1)*(item)}}&nbsp;

            
        </span>
        <span v-else-if="item1>6">
            {{item1+1+5}}X{{item}}={{(item1+1)*(item)}}&nbsp;

  </span>
  <span v-else>
            {{item1+1}}X{{item}}={{(item1+1)*(item)}}&nbsp;
  </span>
  </span>
        </span>
     </span>
  

</template>

<script>
export default {
    data(){
     
    }
}
</script>

<style>
.s{
    text-align: ;
}
</style>