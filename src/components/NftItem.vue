<template>
  <div class="nft-item">
    <img :src="image" :alt="name" />
    <p class="name">{{ name }}</p>
    <p class="description">{{ description }}</p>
    <p class="price">{{ price }}</p>
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.nft-item {
  margin: 20px 0;
  border: 1px solid purple;
  padding: 20px;
  text-align: left;
  background-color: #111;
}

.nft-item img {
  max-width: 100%;
  height: auto;
  border-radius: 16px solid purple;
}

.nft-item .name {
  font-size: 1.5em;
  margin: 10px 0;
  text-align:left;
}

.nft-item .description {
  font-size: 1em;
  margin: 10px 0;
  text-align:left;
}

.nft-item .price {
  font-size: 1.2em;
  color: purple;
  text-align:left;
}
</style>
