<template>
  <h3>Declarative Rendering</h3>
  <div>{{ messege }}</div>
  <button :title="tooltip">Hover Here</button>
  <!-- ======================================= -->
  <hr>

  <h3>Methods</h3>
  <p>{{ count }}</p>
  <button @click="count++">Klik Tambah</button>
  <button @click="addDouble">Tambah Double</button>

  <!-- ============================================== -->
  <hr>
  <h3>V-Model</h3>
  <p style="color: red;">{{ inputText }}</p>
  <input v-model="inputText" />

  <input type="text" :value="inputText" @input="inputText = $event.target.inputText" />
  <!-- ================================== -->
  <hr>
  <h3>Conditional Rendering dengan v-if</h3>
  <div v-if="status">This status TRUE</div>
  <div v-else>This Status FALSE</div>
  <button @click="changeStatus">Change Status</button>


  <!-- ============================================== -->
  <hr>
  <h3>Looping dengan v-for</h3>
  <ol>
    <li v-for="(todo, index) in todos" key="todo.id">
      {{ index }} - {{ todo.activity }}
    </li>
  </ol>


  <!-- ============================================== -->
  <hr>
  <h3>Component Sederhana</h3>
  <ChildComponent/>
</template>
<script>

import ChildComponent from './components/ChildComponent.vue';

export default {
  data() {
    return {
      messege: 'Hallo Vue',
      tooltip: 'This Tooltip',
      count: 0,
      inputText: "",
      status: false,
      status2: true,
      todos: [
        { id: 1, activity: 'Menyapu' },
        { id: 2, activity: 'Makan' },
        { id: 3, activity: 'Minum' },
      ]
    }
  },
  methods: {
    addDouble() {
      this.count = this.count + 5;
    },
    changeStatus() {
      this.status = !this.status
    }
  },
  components:{
    ChildComponent
  }
}
  // name: 'App',
  // components: {
  //   HelloWorld
  // }

</script>


