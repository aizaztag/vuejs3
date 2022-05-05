<template>
  <h1 v-for="name in names" :key="name.firstName">
    <slot name="main" :firstName="name.firstName" :lastName="name.lastName"></slot>
  </h1>
</template>

<script>
export default {
  name: "SlotsProps",
  data() {
    return {
      names: [
        {
          firstName: "One",
          lastName: "Two",
        },
        {
          firstName: "Three",
          lastName: "Fout",
        },
        {
          firstName: "Five",
          lastName: "Six",
        },
      ],
    };
  },
};
</script>
