<template>
    <div class="h-screen w-screen">
        <div class="h-screen w-screen flex flex-col justify-center items-center" id="app">
          <div class = "main-text" @click="onDivClicked">
            <p class="text-4xl font-bold text-gray-800" unselectable="on"> {{ title }} </p>
            <br>
            <div class="font-bold text-emerald-700">{{ message }}</div>
          </div>
            
        </div>
    </div>
    
</template>
<script>
  export default {
    data() {
      return {
        counter: 0,
        list:  [
			"Introduction", 
			"About Me", 
			"Projects", 
			"Contact Me"
		],
		bodyList: [
			"Hey, I'm Neil, an 18 year old developer from California. I am currently studying Computer Science at Purdue University",
			"I'm a full stack developer, and I'm currently working on a few projects.",
			"Here are some of my projects:",
			"Contact me at"
		],
		title: "Introduction",
        message: "Hey, I'm Neil, an 18 year old developer from California. I am currently studying Computer Science at Purdue University"
      }
    },
    methods: {
      onDivClicked: function () {
        if (this.counter < this.list.length - 1) {
          this.counter += 1
        }
        else{
          this.counter = 0
        }
		this.title = this.list[this.counter]
        this.message = this.bodyList[this.counter]
      }
    }
  }
  </script>

