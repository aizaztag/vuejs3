<template>
  <div>
    Article Component
    <br />
    <div v-bind="$attrs">
      {{ title }}
    </div>
    <br />
    {{ status }}<br />
    {{ likes }}<br />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
      default: "Default article title",
    },
    status: Boolean,
    likes: Number,
  },
  inheritAttrrs : Boolean
};
</script>

<style lang="scss" scoped>
</style>