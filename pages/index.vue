<template>
    <div class="h-screen w-screen" @click="onDivClicked">
        <div class="h-screen w-screen flex flex-col justify-center items-center" id="app">
			<Transition name="slide-fade">
				<div class = "main-text" v-if="show">
					<p class="text-4xl font-bold text-gray-800"> {{ title }} </p>
					<br>
					<p class="font-bold text-emerald-700">{{ message }}</p>
					<a class="font-bold text-emerald-800" v-if="counter==2" href="https://github.com/CygnusX-26">Github page</a>
					<p class="font-bold text-emerald-800" v-if="counter==3" >Discord: CygnusX#5667</p>
					<p class="font-bold text-emerald-800" v-if="counter==3">Email: qh4nveh@gmail.com</p>
					<a class="font-bold text-emerald-800" v-if="counter==3" href="https://www.linkedin.com/in/neil-van-eikema-hommes-34b369218/">Linked In</a>
				</div>
			</Transition>
        </div>
    </div>
</template>
<script>
  export default {
    data() {
      return {
        counter: 0,
		show: true,
        list:  [
			"Introduction", 
			"About Me", 
			"Projects", 
			"Get in touch",
		],
		bodyList: [
			"Hey, I'm Neil, an 18 year old developer from California. I am currently studying Computer Science at Purdue University",
			"I'm a full stack developer, and I'm currently working on a few projects.",
			"You can see what I'm working on by visiting my",
			"Contact me at",
		],
		title: "I'm Neil",
        message: "an 18 year old developer from California \ncurrently studying Computer Science at Purdue University.",
      }
    },
    methods: {
      onDivClicked: function () {
		this.show = !this.show;
        if (!this.show) {
          	this.counter ++
        }
        else{
			if (this.counter > this.list.length - 1) {
          		this.counter = 0
			}
        }
		this.title = this.list[this.counter]
        this.message = this.bodyList[this.counter]
      }
    }
  }
  </script>

