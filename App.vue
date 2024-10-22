<template>

  <div id="app">
    <div class="header">
      <h1>Калькулятор роста от Таджика 228 666 69 мега сигма</h1>
     
    </div>

    <div class="container">
      <h2>Калькулятор роста</h2>
      <input v-model="height" type="number" placeholder="Введите ваш рост">
      <button @click="showHeight">Узнать мой рост!</button>

      <div v-if="isModalVisible" class="modal-overlay" @click="closeModal">
        <div class="modal" @click.stop>
          <p>Ваш рост {{ height }} см!!!</p>
          <button @click="closeModal">Закрыть</button>
        </div>
      </div>
    </div>

    <div class="image">
      <img src="https://cdn.leonardo.ai/users/97e57e20-1d7e-4fe0-8dde-23fbef50fcfe/generations/602dfd2b-a1f4-4a13-91f0-56d2741ae525/Leonardo_Phoenix_A_sprawling_dimly_lit_gym_scene_dominated_by_0.jpg">
      <h3>Каждый пользователь, кто использует калькулятор роста стал таким же успешным как мужики сверху</h3>
    </div>
  </div>

  <footer class="footer">
  <p>Разработано Таджиком мега сигмой 666 69 © 2024</p>
  <nav>
    <a href="https://t.me/hochun228" target="_blank" class="telegram-link">
      <img src="https://img.icons8.com/ios-filled/50/000000/telegram-app.png" alt="Telegram Icon" class="telegram-icon">
      Телеграм
    </a>
  </nav>

  <!-- <a href="https://t.me/hochun228" class="footer-button">
    Связаться с нами
  </a>
  <img class="imagefooter" src="https://i.pinimg.com/originals/b2/84/1a/b2841a6f16e2fe3fd98d642f868a6e88.gif"> -->
</footer>

</template>

<script>
export default {
  data() {
    return {
      height: '',
      result: null,
      isModalVisible: false,
      currentIndex: 0,
      images: [
        'https://scribo.kz/wp-content/uploads/2024/03/sigma.webp',
        'https://img.gazeta.ru/files3/213/19018213/00001_-pic_32ratio_1200x800-1200x800-40477.jpg',
        'https://avatars.dzeninfra.ru/get-zen_doc/9632065/pub_6421b26a70ddc014c1c306d4_6421b2fc9ad2261bc2a48db1/scale_1200',
      ],
    };
  },
  methods: {
    showHeight() {
      if (this.height && parseFloat(this.height) > 0) {
        this.isModalVisible = true;
      } else {
        alert("Пожалуйста, введите свой рост.");
      }
    },
    closeModal() {
      this.isModalVisible = false;
    },
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
    },
  },
};
</script>

<style scoped>
 body {
    display: flex;
    flex-direction: column;
    align-items: center; 
    height: 100vh;
    background-color: #e0e0e0;
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
    text-align: center; 
  }
  
  .header {
    margin-bottom: 50px; 
  }
  
  .container {
    margin-top: 40px;
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 300px;
    margin: 100px auto
  }


  .header h1 {
    font-size: 24px; 
    color: black; 
  }

  .header p {
    font-size: 16px;
    font-family: Arial, Helvetica, sans-serif;

  }
  
  h2 {
    color: black;
    font-size: 24px;
    margin-bottom: 20px;
  }
  
 
 input {
    padding: 10px;
    margin: 10px 0;
    width: 100%; 
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 5px;
    outline: none;
    transition: border-color 0.3s;
  }
  
  input:focus {
    border-color: #ff0000;
  }
  
  button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: red;
    border: none;
    border-radius: 5px;
    color: black;
    width: 100%; 
    transition: background-color 0.3s, transform 0.2s;
  }
  
  button:hover {
    background-color: #ff0000;
    transform: translateY(-3px);
  }
  
  button:active {
    transform: translateY(0);
  }
  
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  
  .modal {
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
    text-align: center;
    width: 250px;
  }
  
  .modal p {
    font-size: 18px;
    margin-bottom: 20px;
    color: black;
  }
  
  .modal button {
    padding: 10px 20px;
    background-color: #ff0000;
    border: none;
    border-radius: 5px;
    color: #fff;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .modal button:hover {
    background-color: #ff0000;
  }

.slideshow-container {
  position: relative;
  max-width: 600px; 
  margin: 40px auto; 
}

.slideshow {
  display: flex;
  overflow: hidden; 
  position: relative;
}

.slide {
  min-width: 100%; 
  transition: opacity 0.5s ease; 
  opacity: 0;
}

.slide.active {
  opacity: 1; 
}

img {
  width: 100%; 
  border-radius: 8px; 
}

button.prev, button.next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(255, 255, 255, 0.8);
  border: none;
  border-radius: 50%;
  padding: 10px;
  cursor: pointer;
  font-size: 18px;
}

button.prev {
  left: 10px;
}

button.next {
  right: 10px;
}


  
</style>
