<template>
    <div class="collection-container">
      <h2>NFT Collections</h2>
      <div class="collection-list">
        <a
          class="collection-item"
          v-for="collection in collections"
          :key="collection.name"
          :href="`#${collection.id}`"
        >
          <img :src="collection.image" :alt="collection.name" class="collection-image" />
          <div class="collection-info">
            <h3>{{ collection.name }}</h3>
            <!-- <p>Floor: {{ collection.price }}</p> -->
          </div>
        </a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'NftCollection',
    data() {
      return {
        collections: [
            { id:'Doll' ,image: 'https://img.freepik.com/free-photo/doll-with-fashion-bag_71767-97.jpg?size=626&ext=jpg&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: ' doll Collection', floor: 'Floor: 0.09 ETH' },
          {id:'Cyberpunk' ,image: 'https://img.freepik.com/premium-photo/cyberpunk-cat-portrait-funny-anthropomorphic-animals_739548-3907.jpg?size=626&ext=jpg&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'CyberPunk Collection', floor: 'Floor: 1 ETH' },
          { id:'Monkey' ,image: 'https://img.freepik.com/premium-photo/hiphop-snap-cool-monkey_1164924-10998.jpg?size=626&ext=jpg&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Monkey Collections', floor: 'Floor: 0.01 ETH' },
          { id:'Cartoon' ,image: 'https://img.freepik.com/premium-photo/3d-cartoon-character-3d-happy-cartoon-illustration-3d-cartoon-funny-character-cartoon-kids_1135385-73905.jpg?size=626&ext=jpg&uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: ' Cartoon collection', floor: 'Floor: 0.07 ETH' },
          {id:'Music' , image: 'https://img.freepik.com/free-psd/3d-rendering-dj-character_23-2151437604.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Music collection', floor: 'Floor: 0.05 ETH' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .collection-container {
    padding: 20px;
    background-color: #1a1a1a;
    border-radius: 15px;
    margin: 20px 0;
  }
  
  .collection-container h2 {
    font-size: 2.5em;
    margin-bottom: 20px;
    text-align: center;
    color: #fff;
  }
  
  .collection-list {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
  }
  
  .collection-item {
    background: #2a2a2a;
    border-radius: 15px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    width: 200px;
    text-align: center;
    text-decoration: none;
    color: inherit;
  }
  
  .collection-item:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
  }
  
  .collection-image {
    width: 100%;
    height: auto;
    display: block;
    border-bottom: 2px solid #7e57c2;
  }
  
  .collection-info {
    padding: 15px;
  }
  
  .collection-info h3 {
    margin: 0;
    font-size: 1.2em;
    font-weight: 500;
    color: #fff;
  }
  
  .collection-info p {
    margin: 10px 0;
    font-size: 1em;
    color: #bdbdbd;
  }
  </style>
  