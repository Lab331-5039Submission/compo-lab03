<template>
  <div>
    <div class="organize-card">
      <span>@{{ value.time }} on {{ value.date }}</span>
      <h4>{{ value.category }}</h4>
      <h4>{{ value.organizer }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "OrganizerCard",
  props: {
    value: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.organize-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #727272;
  margin-bottom: 18px;
}
.organize-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
</style>
