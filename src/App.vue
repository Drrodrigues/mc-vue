
<script lang="ts">
import { defineComponent, ref } from 'vue';
import Modal from './Modal.vue';

export default defineComponent({
  components: {
    Modal
  },
  setup() {
    const isModalVisible = ref(false);
    return { isModalVisible };
  }
});

</script>

<template>
   <div className="App">
        <div className='cards'>
          <div className='cardholder'>5545178776051356</div>
          <div>
          </div>
        </div>
        <button variant="primary" @click="isModalVisible = true">
           Buy
        </button>
      
    <Modal v-model:show="isModalVisible">
      <h2>Buy</h2>
      <p>Please confirm your order</p>

       <button variant="secondary" @click="isModalVisible = false">
            Cancel
          </Button>
          <button variant="primary" @click="isModalVisible = false">
            Proceed
          </Button>
    </Modal>
        <div>
    </div>
  </div>
</template>






<style scoped>
.App {
  text-align: center;
  border: black;
  border-style: double;
  border-width: thick;
}

.App-logo {
  height: 40vmin;
  pointer-events: none;
}

@media (prefers-reduced-motion: no-preference) {
  .App-logo {
    animation: App-logo-spin infinite 20s linear;
  }
}

.App-header {
  background-color: #282c34;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: calc(10px + 2vmin);
  color: white;
}

.App-link {
  color: #61dafb;
}

@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.cards {
  border-radius: 25px;
  background: url(/public/card.jpg);
  padding: 20px;
  width: 700px;
  height: 450px;
  margin: auto;
  background-size: cover;
  font-size: x-large;
}

.cardholder {
  color: white;
    margin: auto;
    position: relative;
    top: 300px;
}

.button {
  margin: auto;
}
</style>
