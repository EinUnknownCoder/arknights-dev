<template>
  <v-container>
    <v-row>
      <v-col cols="12" >
        <h2>Sanity Calculator</h2>
      </v-col>

      <v-col cols="12" md="4">
        <v-text-field
          label="Maximum Sanity"
          v-model="maxSanity"
          clearable
          prepend-icon="mdi-head-flash"
        >
        </v-text-field>
      </v-col>

      <v-col cols="12" md="4">
        <v-text-field
          label="Reset Hour"
          v-model="resetHour"
          clearable
          prepend-icon="mdi-hours-24"
        ></v-text-field>
      </v-col>

      <v-col cols="12" md="4">
        <v-alert type="warning" v-if="allowedSanity < maxSanity">Your Sanity should be below {{ allowedSanity }}</v-alert>
        <v-alert type="info" v-else>Spend all your Sanity!</v-alert>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    maxSanity: 128,
    resetHour: 12,
  }),

  computed: {
    allowedSanity() {
      return this.maxSanity - Math.floor(((this.resetHour * 60) - ((new Date().getHours() * 60) + (new Date().getMinutes()))) / 5) + 1
    }
  }
};
</script>
