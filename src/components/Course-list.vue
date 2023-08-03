<template>
  <div>
    <h1>{{ msg }}</h1>
    <p>Course : {{ course.name }}</p>
    <p>Description : {{ course.description }}</p>
    <p>Course ID : {{ course.id }}</p>
    <p>Student #: {{ course.student + count }} / 20</p>
    <button @click="adding">Add</button>
  </div>
</template>

<script>
export default {
  name: "CourseList",
  props: {
    msg: String,
    course: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    adding() {
      this.count++;
    },
  },
};
</script>
