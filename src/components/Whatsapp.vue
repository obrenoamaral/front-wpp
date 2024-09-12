<script>
export default {
  name: 'Whatsapp',
  data() {
    return {
      newMessage: ''
    };
  },
  methods: {
    sendMessage() {
      console.log('Mensagem enviada:', this.newMessage);
      this.newMessage = '';
    }
  }
}
</script>

<template>
  <div class="flex p-10 h-screen w-full bg-gray-900">
    <div class="bg-gray-800 h-auto w-full rounded-lg shadow-lg flex border border-gray-600">
      <div class="flex flex-col items-center h-full bg-gray-800 p-2 rounded-tl-lg rounded-bl-lg border-r border-gray-600">
        <!-- Ícone de Configurações -->
        <div class="mb-4">
          <button class="p-2 rounded-full hover:bg-gray-700 border border-gray-500">
            <!-- Ícone de configuração menor -->
            <svg class="w-6 h-6 text-gray-300" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <circle cx="12" cy="12" r="3"></circle>
              <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51v.28a2 2 0 0 1-2 2h-2a2 2 0 0 1-2-2v-.28a1.65 1.65 0 0 0-1-1.51 1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 1 1-2.83-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2v-2a2 2 0 0 1 2-2h.28a1.65 1.65 0 0 0 1.51-1 1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 1 1 2.83-2.83l.06.06a1.65 1.65 0 0 0 1.82.33h.28a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2v.28a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82v.28a1.65 1.65 0 0 0 1.51 1h.28a2 2 0 0 1 2 2v2a2 2 0 0 1-2 2h-.28a1.65 1.65 0 0 0-1.51 1z"></path>
            </svg>
          </button>
        </div>

        <!-- Foto do Perfil -->
        <div class="mt-auto">
          <img class="w-12 h-12 rounded-full object-cover border border-gray-500" src="/src/assets/bg.png" alt="Profile Picture">
        </div>
      </div>
      <div class="bg-gray-700 w-1/3 h-auto p-4 border-l border-gray-600">
      </div>
      <div class="bg-gray-900 bg-[url('/src/assets/bg.png')] bg-center bg-no-repeat w-2/3 h-auto rounded-tr-lg rounded-br-lg flex flex-col border-l border-gray-600">
        <div class="flex-1 p-4 overflow-y-auto">
          <div v-if="newMessage" class="bg-white text-black p-3 rounded-tl-lg rounded-tr-lg rounded-bl-lg shadow-md w-2/5 ml-auto border border-gray-300">
            {{ newMessage }}
          </div>
        </div>
        <div class="h-20 bg-gray-700 flex items-center p-4 border-t border-gray-600">
          <input
              v-model="newMessage"
              type="text"
              placeholder="Digite uma mensagem..."
              class="w-full h-12 px-4 border border-gray-500 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition-all bg-gray-800 text-white"
          />
          <button
              @click="sendMessage"
              class="ml-2 p-2 bg-green-600 text-white rounded-lg hover:bg-green-500 focus:outline-none focus:ring-2 focus:ring-green-300 transition-all border border-green-700"
          >
            Enviar
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
