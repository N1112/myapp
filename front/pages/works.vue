<template>
  <div>
    <v-col class="text-center">
      <img src="@/assets/image/file.png" class="mb-5" />
    </v-col>
  <time-line></time-line>
  </div>
</template>

<script>
import timeline from "@/components/molecules/timeline.vue";

export default {
  name: "WorksPage",
  components: {
    "time-line": timeline,
  },
  data() {
    return {};
  },
};
</script>
