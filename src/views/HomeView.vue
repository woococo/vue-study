<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <div v-for="alias in items" :key="alias.name">
      <span>{{ alias.name }}</span> : <span>{{ alias.age }}</span><br>
    </div>
    <button @click="btnClick">click me!</button>
    <HelloWorld msg="Welcome to Your Vue.js App" name="남지현" />
  </div>
</template>

<script>
// @ is an alias to /src 
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld
  },
  created() {
    console.log("in created.");
  },
  mounted() {
    console.log("in mounted!");
  },
  beforeUpdate() {
    console.log('in before updated!');
  },
  data () {
    return {
      items: [
        {name: "john", age: 31},
        {name: "tom", age: 12},
        {name: "danny", age: 22},
        {name: "lydia", age: 30},
        {name: "elena", age: 28},
        {name: "judy", age: 22}
      ]
    }
  },  
  methods: {
    btnClick() {
      alert("button clicked!");
    }
  }
};
</script>
