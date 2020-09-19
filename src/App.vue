<template>
  <div class="container mx-16 my-6">
    <h1 class="font-semibold">hello {{name}} and {{greet('afternoon')}}</h1>
    <button
      class="text-purple-500 hover:text-white hover:bg-purple-500 border border-purple-500 text-sm font-semibold rounded-full px-4 py-1 leading-normal"
      @click="increase(10)"
    >increase</button>
    <p class="font-semibold">my age is: {{age}}</p>
    <button
      class="text-purple-500 hover:text-white hover:bg-purple-500 border border-purple-500 text-sm font-semibold rounded-full px-4 py-1 leading-normal"
      @click="decrease(10)"
    >decrease</button>
    <a class="block" :href="website">my awesome site o</a>
    <input
      type="text"
      :value="name"
      class="border border-purple-400 rounded-lg pl-2 focus:border-none"
    />
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
    };
  },
  methods: {
    greet(time) {
      return `good ${time} sir`;
    },
    increase(increment) {
      this.age += increment;
    },
    decrease(decrement) {
      this.age -= decrement;
    },
  },
};
</script>

