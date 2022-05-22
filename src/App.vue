<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 v-show="Resources.isVisible/*isVisible*/">{{ Resources.CourseGoal /*CourseGoal*/ }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="toggleGoal">{{ /*isVisible*/ Resources.isVisible  ? 'Hide ' : 'Show ' }}Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

//Compositions API
<script setup>
import { ref, reactive } from 'vue';
// Using separate Refs
// const CourseGoal = ref('Complete Vue');
// const isVisible = ref(true);

// Using Ref object
// const Resources = ref({
//   CourseGoal: 'Complete Vue',
//   isVisible: true,
// });

// Using Reactive
const Resources = reactive({
  CourseGoal: 'Complete Vue',
  isVisible: true,
});

function toggleGoal(){
  // return isVisible = !isVisible;
  // return Resources.value.isVisible = !Resources.value.isVisible;
  return Resources.isVisible = !Resources.isVisible;
}
</script>

<!-- //Options API
<script>
export default {
  data(){
    return {
      CourseGoal: 'Complete Vue',
      isVisible: true,
    };
  },
  methods:{
    toggleGoal(){
      return this.isVisible = ! this.isVisible;
    }
  },
}
</script> -->

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>