<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <CourseList
    msg="List of Courses"
    v-for="course in courses"
    :key="course.name"
    :course="course"
  />
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import CourseList from "./components/Course-list.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    CourseList,
  },

  data() {
    return {
      count: 0,
      courses: [
        {
          name: "Math",
          description: "Learn to add number",
          id: 1,
          student: 15,
        },
        { name: "Science", description: "What is this", id: 2, student: 10 },
        {
          name: "French",
          description: "Can you say Bonjour",
          id: 3,
          student: 5,
        },
      ],
    };
  },
  methods: {
    addOne() {
      this.count++;
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
div {
  border: #2c3e50 2px solid;
}
</style>
