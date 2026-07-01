<script setup>
import { reactive, ref, computed, watch } from "vue";
const firstName = ref("bhasgkar");
const lastName = ref("gupta");
const fullName = computed(() => firstName.value + " " + lastName.value);
import parent from "./parent.vue";
// let initialState = reactive({ count: 0 });

// let count = ref(0)
// const myMessage = " Hello World ";
// const myNumber = 100;
// const add = (x, y) => x + y;

// const myChannel = "https://www.youtube.com/watch?v=ymXJlPeM-qI";
// const image =
//   "https://images.unsplash.com/photo-1454496522488-7a8e488e8606?ixid=M3w4MjcwNjd8MHwxfHNlYXJjaHwzfHxtb3VudGFpbnN8ZW58MHx8fHwxNzgyODIyODQxfDA&ixlib=rb-4.1.0&fit=max&q=80";
// const altText = "This is a random picture";
// const imgWidth = 400;
// const imgHeight = 400;
</script>

<template>
  <div>
    <!-- <h1>{{ myMessage }}</h1> -->
    <h1>{{ fullName }}</h1>
<parent/>
    <!-- ref us used t ocr3ate a reacitve referece to a val<ue
unlinke reactive function, which is used for creating reactive objects,
ref us specifically designed for creating reeactive single values
you can store any value you want even primitive
 -->
<!-- 
    Computer properties special kinnd of variable that automatcally updates
    itself whenever the data it depends on changesit it's like a little worker
    that watches certian data, performs some work on it, and always gies you
    most up-to data result -->

    <!-- <h1>{{ myNumber }}</h1>
    <h1>2 + 2 = {{ 2 + 2 }}</h1>
    <h1>Adding two numbers: {{ add(2, 2) }}</h1>
    <h1>count: {{ initialState.count }}</h1>
    <button @click="
        initialState.count++
    ">Increment</button>
    <button @click="
        initialState.count--
    ">Decrement</button> -->

    <!-- <a :href="myChannel">His Channel</a>
    <img :src="image" :alt="altText" :width="imgWidth" :height="imgHeight" / >

    reactive() if a function used to create reactive object what are these
    reactive objects, reactive objects is a oject which changesit's properties
    are automatcally detected, triggreing updagtes in the user iterface way to
    make an object reativein vue js can't store primitive data types ref() -->

    <!-- we cannot declare a variable inside {{  }} -->

    <!-- Conditional Rendering
    refers to the abiity to conditionally display or hide element in
    the UI based on certain conditions or expressions
    -->








  </div>
</template>
