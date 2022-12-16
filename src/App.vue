<template>
  <div>{{messege}}</div>
  <button :title="tooltip">Hover Here</button>
</template>
<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  data(){
    return{
      messege: 'Hallo Vue',
      tooltip: 'This Tooltip'
    }
  }
  // name: 'App',
  // components: {
  //   HelloWorld
  // }

}</script>


