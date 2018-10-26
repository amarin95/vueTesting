<template>
  <div class="about">
    <h1>This is an about page</h1>
      <aplayer :music="{
    title: 'secret base~君がくれたもの~',
    artist: 'Silent Siren',
    src: 'https://moeplayer.b0.upaiyun.com/aplayer/secretbase.mp3',
    pic: 'https://moeplayer.b0.upaiyun.com/aplayer/secretbase.jpg'
  }"
      />
  </div>

</template>

<script>
    // @ is an alias to /src
    import HelloWorld from '@/components/HelloWorld.vue'
    import Todo from "../components/todo";
    import Aplayer from 'vue-aplayer';

    export default {
        name: 'home',
        components: {
            Todo,
            HelloWorld,
            Aplayer

        }
    }
</script>
