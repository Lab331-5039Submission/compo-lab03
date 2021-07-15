<template>
  <div>
    <div class="student-card">
      <img :src="student.image" :alt="student.name" width="200" />
      <p>{{ student.id }}</p>
      <h4>{{ student.name }} {{ student.surname }}</h4>
      <h4>{{ student.gpa }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "StudentCard",
  props: {
    student: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.student-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #727272;
  margin-bottom: 18px;
}
.student-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
</style>
