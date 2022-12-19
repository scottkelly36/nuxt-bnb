<template>
    <v-row>
        <v-col
          cols="12"
          sm="6"
        >
          <v-date-picker
            v-model="dates"
            range
            header-color="var(--blue)"
            color="var(--blue)"
          ></v-date-picker>
        </v-col>
        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            v-model="dateRangeText"
            label="Date range"
            prepend-icon="mdi-calendar"
            readonly
          ></v-text-field>
          {{ dates }}
        </v-col>
      </v-row>
</template>

<script>
export default {
    data: () => ({
      dates: [],
    }),
    computed: {
      dateRangeText () {
        return this.dates.join(' ~ ')
      },
    },
}
</script>

<style>

</style>