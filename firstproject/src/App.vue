<!-- Options API -->
<!-- 
<script>
export default {
  data() {
    return {
      name: "John Doe",
      status: false,
      tasks: ["Task One", "Task Two", "Task Three"],
      link: "https://google.com",
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === "active") {
        this.status = "pending";
      } else if (this.status === "pending") {
        this.status = "inactive";
      } else {
        this.status = "active";
      }
    },
  },
};
</script> -->

<!-- composition api -->
<!-- 
<script setup>
import { ref } from "vue";
const name = ref("john doe");
const status = ref("active");
const tasks = ref(["task one", "task two"]);
const newTask = ref("");
const link = ref("https://google.com");

const toggleStatus = () => {
  if (status.value === "active") {
    status.value = "pending";
  } else if (status.value === "pending") {
    status.value = "inactive";
  } else {
    status.value = "active";
  }
};
</script>

<template>
  <h1>Bhaskar Gupta</h1>
  <h2>{{ name }}</h2>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <form @submit.prevent="addTask">
    <label for="newTask">Add Task</label>
    <input type="text" id="newTask" v-model="newTask" />
  </form>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li> -->
<!-- key is used to be just more accurate -->
<!-- </ul>
  <!-- <a v-bind:href="link"></a>  or -->
<!-- <a :href="link">Click For Google</a>

  <button v-on:click="toggleStatus">Change Status</button> -->
<!-- or -->
<!-- <button @click="toggleStatus">Change Status</button>
</template>

<style scoped>
h1 {
  color: red;
}
h2 {
  color: blue;
}
</style> -->
<!-- // used for styling here and scoped
 means onlyapply that fucntion only on thsi component -->

<script setup>
import { ref, onMounted } from 'vue'

const name = ref("John Doe");
const status = ref("active");
const tasks = ref(["Task One", "Task Two", "Task Three"]);
const newTask = ref("");
const link = ref("https://google.com");

function toggleStatus() {
  if (status.value === "active") {
    status.value = "pending";
  } else if (status.value === "pending") {
    status.value = "inactive";
  } else {
    status.value = "active";
  }
}

function addTask() {
  if (newTask.value.trim() !== "") {
    tasks.value.push(newTask.value);
    newTask.value = "";
  }
}

const deleteTask = (index) => {
  tasks.value.splice(index, 1);
};

onMounted(async ()=>{
  try{
    
    const response = await fetch('https://jsonplaceholder.typicode.com/todos');
    const data = await response.json();
    tasks.value = data.map((task)=> task.title);
  
  
  
  
  } catch(error){
    console.log('Error Ferching Tasks');
  }
});


</script>

<template>
  <h1>Bhaskar Gupta</h1>
  <h2>{{ name }}</h2>

  <p v-if="status === 'active'">User is active</p>

  <p v-else-if="status === 'pending'">User is pending</p>

  <p v-else>User is inactive</p>

  <form @submit.prevent="addTask">
    <label for="newTask">Add Task</label>

    <input type="text" id="newTask" v-model="newTask" />
    <button type="submit">Submit</button>
  </form>

  <h3>Tasks:</h3>

  <ul>
    <li v-for="{ task, index } in tasks" :key="task">
      <span>
        {{ task }}
      </span>
      <button @click="deleteTask(index)">X</button>
    </li>
  </ul>

  <a :href="link">Click For Google</a>

  <button @click="toggleStatus">Change Status</button>
</template>








<!-- Now Learning About Lifecycle Methods  -->
 <!-- onBeforeMount
 onMounting
  -->