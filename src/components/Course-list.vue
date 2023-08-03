<template>
  <div>
    <h1>{{ msg }}</h1>
    <p>Course : {{ course.name }}</p>
    <p>Description : {{ course.description }}</p>
    <p>Course ID : {{ course.id }}</p>
    <p>Student #: {{ course.student + count }} / 20</p>
    <button :class="av" v-if="availability" @click="adding">Add</button>
    <button :class="nav" v-else @click="minus">Remove</button>
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
      av: "av-label",
      nav: "av-label disabled",
      availability: true,
    };
  },
  methods: {
    adding() {
      this.count++;
    },
    minus() {
      this.count--;
    },
  },
};
</script>
