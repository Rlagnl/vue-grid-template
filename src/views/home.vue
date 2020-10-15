<template>
  <div class="home-wrapper">
    <div class='item'><p>1</p></div>
    <div class='item'><p>2</p></div>
    <div class='item'><p>3</p></div>
    <div class='item'><p>4</p></div>
    <div class='item'><p>5</p></div>
    <div class='item'><p>6</p></div>
    <div class='item'><p>7</p></div>
    <div class='item'><p>8</p></div>
    <div class='item'><p>9</p></div>
  </div>
</template>

<script lang='ts'>
import vue from 'vue'
import Component from 'vue-class-component'
import HelloWorld from '../components/HelloWorld.vue'
import logoImage from '../assets/images/logo.png'

@Component ({
  components: {
    HelloWorld
  }
})
export default class App extends vue{
  private logoImage: string = logoImage
}
</script>

<style>
.home-wrapper {
  width: 300px;
  height: 300px;
  background-color: bisque;
  display: grid;

  /* repeat(3, 33.33%); | 100px 100px 100px */
  grid-template-columns: repeat(auto-fill, 1fr);
  grid-template-rows: repeat(auto-fill, 1fr);

  /* grid-row-gap: 20px;
  grid-column-gap: 20px; */
  gap: 20px;

  grid-template-areas: 'a a a'
                      'b b b'
                      'c c c';
  /* column | row */
  /* grid-auto-flow: column; */

  /* start | end | center | stretch */
  /* justify-items: start; */
  /* align-items: start; */
  /* place-items: start start; */

  /* start | end | center | stretch | space-around | space-between | space-evenly */
  /* justify-content: start;
  align-content: start; */
  /* place-content: start; */
}
.item {
  background-color: orange;
}
.item:nth-child(1) {
  /* grid-column-start: 2;
  grid-column-end: 4;
  grid-column: 2 / 4; */
  grid-area: b;
}
</style>
