<template>
  <div class="options-container">
    <ul>
      <li
        v-for="sticker in stickers"
        :key="sticker.id"
        @click="$emit('selection', sticker.id,) "
      >
        {{ sticker.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    stickers: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
}

li {
  background-color: white;
  border-radius: 5px;
  border: 1px solid rgba(0, 0, 0, 0.2);
  cursor: pointer;
  margin-bottom: 10px;
  width: 250px;
  font-family: "Press Start 2P", cursive;
  font-size: 12px;
}

li:hover {
  background-color: rgba(0, 0, 0, 0.05);
}

.options-container {
  display: flex;
  justify-content: center;
}
</style>