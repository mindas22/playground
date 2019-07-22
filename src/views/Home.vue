<template>
  <div class="home">
<h1>{{h1}}</h1>
<h2>it will be here: {{h2}} </h2>
<ul>
  <li v-for="something in items" :key="something">{{something.text}}</li>
</ul>
<input type="text" v-model="h2" name="itemname" id="itemname"><br>
<button @click="changeh3()">press me</button>

<h3 v-if="h3">hello how are you? </h3>

<item2 v-model="h2.value" />

  </div>
</template>

<script>
// @ is an alias to /src
import item2 from "@/components/item2.vue";

export default {
  data () {
    return {
      items: [
        {text: "item one"},
        {text: "item two"},
        {text: "item three"},
        {text: "item 4"}
      ],
      h1: "it is nothing here two",
      h2: "mmm",
      h3: true
    }
  },
  methods: {
    changeh3() {
      this.h3 = !this.h3
    }
  },
  components: {
    item2
  }
}
</script>
