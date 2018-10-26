<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <todo></todo>
      <aplayer :music="{
    title: 'secret base~君がくれたもの~',
    artist: 'Silent Siren',
    src: 'https://moeplayer.b0.upaiyun.com/aplayer/secretbase.mp3',
    pic: 'https://moeplayer.b0.upaiyun.com/aplayer/secretbase.jpg'
  }"
      />
      <p>{{count}}</p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    <div>
      <p>El resultado guardado de la calculadora es: {{result}}</p>
    </div>
  </div>

</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Todo from "../components/todo";
import Aplayer from 'vue-aplayer';
import Store from '../store'

export default {
  name: 'home',
  components: {
      Todo,
    HelloWorld,
      Aplayer

  },
    computed:{
        count () {
            return Store.state.count;
        },
        result(){
            return Store.state.result;
        }
    },
  methods:{
      increment () {
          Store.commit('increment')
      },
      decrement () {
          Store.commit('decrement')
      }
  }
}
</script>
