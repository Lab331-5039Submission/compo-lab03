<template>
  <h1>Organizer List only</h1>
  <hr />
  <div class="organize">
    <OrganizerCard v-for="event in events" :key="event.id" :value="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import OrganizerCard from "@/components/OrganizerCard.vue"
import EventService from "@/service/EventService.js"
export default {
  name: "OrganizerOnly",
  components: {
    OrganizerCard
  },
  data() {
    return {
      events: null
    }
  },
  created() {
    EventService.getEvents().then((res) => {
      this.events = res.data
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
