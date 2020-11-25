<template>
  <div class="heavy-nested-block">
    <HeavyNestedBlock v-if="iterations > 0" :iterations="iterations - 1" :text="text" />
    <div v-else class="heavy-nested-block__content">
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeavyNestedBlock',
  props: {
    iterations: {
      type: Number,
      default: 0
    },
    text: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
.heavy-nested-block {
  margin: 1px;
  padding: 1px;
  border: 1px solid #dedede;
  font-size: 10px;
  line-height: 10px;
}
</style>