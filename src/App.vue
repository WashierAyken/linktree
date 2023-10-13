<template>
  <div id="app" class="app">
    <h1 class="title">Mi Linktree</h1>
    <div class="link-container">
      <a v-for="link in links" :key="link.text" :href="link.url" class="link" target="_blank">
        <i class="fas fa-external-link-alt"></i> {{ link.text }}
      </a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      links: [
        { text: "Linkedin", url: "http://www.linkedin.com/in/isaactovias" },
        { text: "Twitch", url: "http://www.twitch.tv/donayken" },
        {text: "Twitter", url:"http://www.twitter.com/illojuan"},
        // Agrega más enlaces si es necesario
      ],
    };
  },
};
</script>

<style scoped>
/* Estilos modernos */
h1{
  color: #1e1e1e;
}

.app {
  max-width: 360px;
  margin: 0 auto;
  padding: 20px;
  font-family: Arial, sans-serif;
  text-align: center;
  background: linear-gradient(to bottom, #6a3093, #a044ff);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  border-radius: 8px;
  display: flex;
  flex-direction: column;
}
.title {
  font-size: 28px; 
  margin-bottom: 20px;
  color: #474242;

}

.link-container {
  display: flex;
  text-align: center;

}

.link {
  text-decoration: none;
  color: #333;
  display: block;
  padding: 12px; 
  margin: 120px; 
  background: #0070f3;
  color: #fff;
  border-radius: 4px;
  transition: background-color 0.3s ease, transform 0.2s ease;
  font-size: 16px; 
  font-weight: 600;
  

}

.link:hover {
  background-color: #0050c8;
  transform: scale(1.05);
  
  
}
</style>
