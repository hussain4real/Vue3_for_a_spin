<template>
  <div id="app" class="container mx-16 my-6">
    <h1 class="font-semibold">hello {{name}} and {{greet('day')}}</h1>
    <button
      class="text-purple-500 hover:text-white hover:bg-purple-500 border border-purple-500 text-sm font-semibold rounded-full px-4 py-1 leading-normal"
      @click="increase(1)"
    >increase</button>
    <button
      class="text-purple-500 hover:text-white hover:bg-purple-500 border border-purple-500 text-sm font-semibold rounded-full px-4 py-1 leading-normal"
      @dblclick="increase(10)"
    >increase2x</button>
    <p class="font-semibold">age is: {{age}}</p>
    <button
      class="text-purple-500 hover:text-white hover:bg-purple-500 border border-purple-500 text-sm font-semibold rounded-full px-4 py-1 leading-normal"
      @click="decrease(1)"
    >decrease</button>
    <button
      class="text-purple-500 hover:text-white hover:bg-purple-500 border border-purple-500 text-sm font-semibold rounded-full px-4 py-1 leading-normal"
      @dblclick="decrease(10)"
    >decrease2x</button>
    <a class="block" :href="website">my awesome site</a>
    <input
      type="text"
      :value="name"
      class="border border-purple-400 rounded-lg pl-2 focus:border-none"
    />
  </div>
  <div class="w-3/4">
    <p
      id="canvas"
      class="border rounded-md border-black ml-6 py-32 text-center"
      @mousemove="updateXY"
    >{{x}}, {{y}}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Hussain",
      age: 27,
      website: "https://twitter.com",
      x: 0,
      y: 0,
    };
  },
  methods: {
    greet(time) {
      return `good ${time} sir`;
    },
    increase(increment) {
      setTimeout(() => {
        this.age += increment;
      }, 1000);
    },
    decrease(decrement) {
      this.age -= decrement;
    },
    updateXY(event) {
      this.x = event.offsetX;
      this.y = event.offsetY;
    },
  },
};
</script>



