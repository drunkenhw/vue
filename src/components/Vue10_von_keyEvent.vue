<template>
  <h1>v-on key event</h1>
  <!-- <input type="submit" value="Send" v-on:keyup.enter="send"> -->
  <input type="submit" value="Send" v-on="{ 'keyup.enter':send, click:send }"><br>
  enter키와 클릭할 때 반응
  
  <input type="text" v-on:keyup='keyPressed1($event)'><br>
  모든 키 반응 String.fromCharCode()으로 숫자와 알파벳만 문자로 변환

  <input type="text" v-on:keyup.page-down='keyPressed2($event,"Page Down")'><br>
  String.fromCharCode() 미적용 특정키 만 반응(page down)

  <input type="text" v-on:keyup.exact.alt.shift="onMix1"
    v-on:keyup.exact.page-up="onMix2"> <br>
  alt shift exact, page-up exact

  <input type="text" v-on:keyup.exact.alt.shift="onMix1"
    v-on:keyup.page-up="onMix2"> <br>
  alt shift exact, page-up no

  <input type="text" v-on:keyup.alt.shift="onMix1"
    v-on:keyup.exact.page-up="onMix2"> <br>
  alt shift no, page-up exact     
  
  alt shift no, page-up no => not working<br>
  <!-- <input type="text" v-on:keyup.alt.shift="onMix1" v-on:keyup.page-up="onMix2"> -->

  <input type="text" v-on:keyup.meta="onMeta"> meta

</template>

<script>
export default {
  methods: {
    send() {console.log('enter key가 눌러졌습니다.')},
    keyPressed1(e) {console.log(String.fromCharCode(e.keyCode)+' is pressed')},
    keyPressed2(e,caption) {console.log(caption+"("+(e.keyCode)+') is pressed')},
    onMix1() {console.log("1복합 클릭했어요");},
    onMix2() {console.log("2복합 클릭했어요");},
    onMeta() {console.log("윈도우키를 누르고 키를 눌렀어요");},
  }
}
</script>

<style>

</style>