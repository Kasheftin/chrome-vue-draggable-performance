<template>
  <div class="container" v-dragscroll>
    <div class="settings">
      Items Count:
      <input v-model.lazy="itemsCount">
    </div>
    <div class="list">
      <div 
        v-for="n in Number(itemsCount)" 
        :key="n" 
        class="list-item"
      >
        <div class="block">
          {{ text }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin accumsan pellentesque hendrerit. Ut dignissim ex massa, sit amet sodales nunc accumsan ut. Duis a urna erat. Donec eros ante, bibendum non mauris eget, porta pulvinar turpis. Etiam elementum mattis magna id scelerisque. Sed eget magna posuere, blandit odio ut, rutrum dui. Proin dapibus urna mi. Maecenas at finibus libero. Maecenas enim sem, imperdiet nec turpis ac, varius imperdiet ex. Sed at venenatis urna, rhoncus convallis ipsum.',
      itemsCount: 10000
    }
  }
}
</script>

<style scoped>
.container {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  overflow: auto;
}
.list {
  width: 3000px;
  height: 300000px;
  position: relative;
  padding: 50px;
}
.list-item {
  margin: 20px;
  width: 800px;
}
.block {
  margin: 1px;
  padding: 1px;
  border: 1px solid #dedede;
  font-size: 10px;
  line-height: 10px;
}
.settings {
  position: fixed;
  display: flex;
  align-items: center;
  padding: 10px;
  background-color: #f0f0f0;
  box-shadow: 3px 3px 3px rgba(0, 0, 0, 0.2);
  z-index: 2;
}
.settings input {
  margin: 0 15px 0 5px;
}
</style>