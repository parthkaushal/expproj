<template>
  <v-timeline>
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :color="year.color"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <div class="py-4">
        <h2 :class="`headline font-weight-light mb-4 ${year.color}--text`">Srila Prabhupada</h2>
        <div>
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'cyan',
          year: '1896',
        },
        {
          color: 'green',
          year: '1922',
        },
        {
          color: 'pink',
          year: '1933',
        },
        {
          color: 'amber',
          year: '1944',
        },
        {
          color: 'orange',
          year: '1951',
        },
        {
          color: 'blue',
          year: '1959',
        },
        {
          color: 'teal',
          year: '1962',
        },
        {
          color: 'purple',
          year: '1965',
        },
        {
          color: 'pink',
          year: '1966',
        },
        {
          color: 'red',
          year: '1977',
        },
      ],
    }),
  }
</script>