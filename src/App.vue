<template>
  <div id="app">
    <header class="header">
      <div class="header-content">
        <h1>NFT Collection</h1>
        <p>
          Explore the unique and high-quality digital paintings of the NFT collection.
        </p>
      </div>
      <NftCollection />
    </header>
    <section id="Monkey" class="nft-collection">
      <h2>Monkey Collection</h2>
      <NftItem
        v-for="(nft, index) in nfts.filter(nft => nft.id === 'Monkey')"
        :key="index"
        :image="nft.image"
        :name="nft.name"
        :description="nft.description"
        :price="nft.price"
      />
    </section>
    <section id="Doll" class="nft-collection">
      <h2>Doll Collection</h2>
      <NftItem
        v-for="(nft, index) in nfts.filter(nft => nft.id === 'Doll')"
        :key="index"
        :image="nft.image"
        :name="nft.name"
        :description="nft.description"
        :price="nft.price"
      />
    </section>
    <section id="Cyberpunk" class="nft-collection">
      <h2>CyberPunk Collection</h2>
      <NftItem
        v-for="(nft, index) in nfts.filter(nft => nft.id === 'Cyberpunk')"
        :key="index"
        :image="nft.image"
        :name="nft.name"
        :description="nft.description"
        :price="nft.price"
      />
    </section>
    <section id="Cartoon" class="nft-collection">
      <h2>Cartoon Collection</h2>
      <NftItem
        v-for="(nft, index) in nfts.filter(nft => nft.id === 'Cartoon')"
        :key="index"
        :image="nft.image"
        :name="nft.name"
        :description="nft.description"
        :price="nft.price"
      />
    </section>
    <section id="Music" class="nft-collection">
      <h2>Music Collection</h2>
      <NftItem
        v-for="(nft, index) in nfts.filter(nft => nft.id === 'Music')"
        :key="index"
        :image="nft.image"
        :name="nft.name"
        :description="nft.description"
        :price="nft.price"
      />
    </section>
  </div>
</template>

<script>
import NftCollection from './components/NftCollection.vue';
import NftItem from './components/NftItem.vue';

export default {
  name: 'App',
  components: {
    NftItem,
    NftCollection,
  },
  data() {
    return {
      nfts: [
        { id: 'Monkey', image: 'https://img.freepik.com/premium-photo/gorilla-painted-wall-with-green-purple-background_869640-142421.jpg?size=626&ext=jpg&uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Monkey Gif 2', description: 'This image features a vibrant, graffiti-style mural of a gorilla painted on a brick wall', price: '1.5 ETH' },
        { id: 'Monkey', image: 'https://media1.tenor.com/m/WXfV9SHYx8YAAAAC/monkey-blink.gif', name: 'Cap Monkey', description: 'An engaging animated NFT featuring a playful monkey with a cap. Perfect for collectors looking for a touch of fun and charm in their digital collection.', price: '1.2 ETH' },
        { id: 'Doll', image: 'https://img.freepik.com/premium-photo/cyberpunk-dolls_378362-1380.jpg', name: 'Cyberpunk Doll', description: 'This image features cyberpunk-style dolls, showcasing a futuristic and stylized interpretation of humanoid figures often associated with cyberpunk aesthetics.', price: '1.0 ETH' },
        { id: 'Doll', image: 'https://img.freepik.com/premium-photo/handmade-skull-type-gothic-rag-doll-halloween-night-mystery-digital-painting-background-illustration_285885-875.jpg', name: 'Skull Doll', description: 'This image depicts a handmade skull-type Gothic rag doll against a Halloween night mystery backdrop, digitally painted for an eerie and atmospheric illustration.', price: '1.8 ETH' },
        { id: 'Cyberpunk', image: 'https://img.freepik.com/free-photo/portrait-sheep-cyberpunk-style_23-2151195553.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'sheep Cyberpunk ', description: 'This image shows a portrait of a sheep in cyberpunk style, blending futuristic elements with the natural appearance of the animal, creating a unique and surreal visual contrast.', price: '2.5 ETH' },
        { id: 'Cyberpunk', image: 'https://img.freepik.com/premium-photo/neon-city-cyberpunk-woman_1115474-35351.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Cyberpunk Woman', description: 'This image features a cyberpunk woman in a neon-lit cityscape, embodying the futuristic and vibrant aesthetic often associated with cyberpunk culture.', price: '3.0 ETH' },
        { id: 'Cartoon', image: 'https://img.freepik.com/premium-photo/cartoon-character-with-jacket-that-says-i-m-robot_784625-11260.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Boy Cartoon ', description: 'This image portrays a cartoon character wearing a jacket that says "Im Robot," combining a playful cartoon style with a futuristic theme, suggesting a character with robotic or cybernetic elements.', price: '0.9 ETH' },
        { id: 'Cartoon', image: 'https://img.freepik.com/premium-photo/3d-cartoon-character-3d-happy-cartoon-illustration-3d-cartoon-funny-character-cartoon-kids_1135385-90227.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Happy Cartoon', description: 'This image showcases a 3D cartoon character, designed with a happy and humorous expression typical of childrens cartoons, featuring vibrant colors and a playful demeanor.', price: '1.4 ETH' },
        { id: 'Music', image: 'https://img.freepik.com/premium-photo/woman-with-purple-glasses-purple-glasses-is-painting-woman-wearing-goggles_928869-53461.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'purple glass', description: 'This image depicts a woman wearing purple glasses and goggles, engaged in painting or creative work, emphasizing her artistic expression and unique style.', price: '2.2 ETH' },
        { id: 'Music', image: 'https://img.freepik.com/premium-vector/cheerful-cool-llama-dj-console-with-headphones-hot-party_74747-27.jpg?uid=R130401869&ga=GA1.1.1852814725.1717767020&semt=ais_user', name: 'Llama Dj', description: 'This image features a cheerful llama DJ with headphones, spinning tunes at a hot party, embodying a lively and fun atmosphere with its cool and quirky persona.', price: '2.8 ETH' },
      ],
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: 'Roboto', sans-serif;
  background-color: #000000;
  color: #fff;
  border-radius: 15px;
}

header {
  padding: 50px;
  text-align: center;
  background: linear-gradient(145deg, #2a2a2a, #1a1a1a);
  border-bottom: 2px solid #52057B;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
  border-radius: 0 0 15px 15px;
}

header h1 {
  font-size: 2.5em;
  font-weight: 700;
  margin-bottom: 20px;
}

header p {
  font-size: 1.2em;
  font-weight: 300;
  color: #bdbdbd;
}

.nft-collection {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  padding: 20px;
  margin: 40px 0;
  position: relative;
}

.nft-collection h2 {
  width: 100%;
  font-size: 2em;
  text-align: center;
  margin-bottom: 20px;
  color: #fff;
}

.nft-collection:not(:last-of-type)::after {
  content: '';
  display: block;
  width: 100%;
  height: 2px;
  background: #52057B;
  position: absolute;
  bottom: -20px;
  left: 0;
  margin: 0 20px;
}

.nft-item {
  background: #1e1e1e;
  border-radius: 15px;
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.nft-item:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
}

.nft-image {
  width: 100%;
  height: auto;
  display: block;
  border-bottom: 2px solid #7e57c2;
  border-radius: 15px 15px 0 0;
}

.nft-info {
  padding: 15px;
}

.nft-info h3 {
  margin: 0;
  font-size: 1.5em;
  font-weight: 500;
}

.nft-info p {
  margin: 10px 0;
  font-size: 1em;
  color: #bdbdbd;
}

.price {
  font-size: 1.2em;
  color: #7e57c2;
  font-weight: 500;
}
</style>
