<template>
  <h3>Declarative Rendering</h3>
  <div>{{ messege }}</div>
  <button :title="tooltip">Hover Here</button>

  <hr>

  <h3>Methods</h3>
  <p>{{ count }}</p>
  <button @click="count++">Klik Tambah</button>
  <button @click="addDouble">Tambah Double</button>

</template>
<script>

export default {
  data() {
    return {
      messege: 'Hallo Vue',
      tooltip: 'This Tooltip',
      count: 0
    }
  },
  methods:{
    addDouble(){
      this.count = this.count + 5;
    }
  }
}
  // name: 'App',
  // components: {
  //   HelloWorld
  // }

</script>


