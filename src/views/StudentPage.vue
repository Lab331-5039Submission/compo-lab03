<template>
  <h1>List of all Student</h1>
  <hr />
  <div class="organize">
    <StudentCard v-for="item in students" :key="item.id" :student="item" />
  </div>
</template>

<script>
// @ is an alias to /src
import StudentCard from "@/components/StudentCard.vue"
import StudentAPI from "@/service/StudentAPI.js"
export default {
  name: "OrganizerOnly",
  components: {
    StudentCard
  },
  data() {
    return {
      students: null
    }
  },
  created() {
    StudentAPI.getStudent().then((res) => {
      this.students = res.data
    })
  }
}
</script>
<style scoped>
.organize {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
