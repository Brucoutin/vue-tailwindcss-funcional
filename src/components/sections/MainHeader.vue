<template>
  <div class="bg-white py-4">
    <div class="container mx-auto flex justify-between items-center px-4">
      <div class="flex items-center">
        <div class="w-32 h-16 flex items-center justify-center">
          <img :src="governopara" alt="Logo DETRAN PA" class="w-80" />
        </div>
      </div>

      <div class="hidden md:flex flex-1 justify-center px-4">
        <div class="relative w-full max-w-xl">
          <input type="text" placeholder="Buscar no site..."
            class="w-full bg-gray-50 px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" />
          <svg class="absolute right-3 top-1/2 transform -translate-y-1/2 w-5 h-5 text-gray-400" fill="currentColor"
            viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd"
              d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
              clip-rule="evenodd" />
          </svg>
        </div>
      </div>

      <div class="hidden md:flex items-center space-x-6">
        <a href="#" class="text-vermelho font-bold fonte-principal hover:underline">Agência Pará</a>
        <a href="#" class="text-vermelho font-bold fonte-principal hover:underline">Portal do Servidor</a>
        <div class="w-32 h-16 flex items-center justify-center">
          <img :src="governopara" alt="Logo DETRAN PA" class="w-80" />
        </div>
      </div>

      <button @click="toggleMobileMenu" class="md:hidden text-gray-800 hover:text-blue-800 focus:outline-none">
        <svg v-if="!isMobileMenuOpen" class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
        <svg v-else class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
    </div>
  </div>
  <div v-if="isMobileMenuOpen" class="md:hidden bg-azul text-white p-4">
    <div class="flex flex-col space-y-2">
      <a href="#" class="text-white font-bold fonte-principal hover:underline py-2">Agência Pará</a>
      <a href="#" class="text-white font-bold fonte-principal hover:underline py-2">Portal do Servidor</a>
      <div class="flex items-center space-x-2 py-2">
        <a href="#" class="text-white hover:text-cinza">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd"
              d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
              clip-rule="evenodd" />
          </svg>
        </a>
        <a href="#" class="text-white hover:text-cinza">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.71v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" />
          </svg>
        </a>
        <a href="#" class="text-white hover:text-cinza">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd"
              d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.024.06 1.378.06 3.808s-.012 2.784-.06 3.808c-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.024.048-1.378.06-3.808.06s-2.784-.013-3.808-.06c-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.048-1.024-.06-1.378-.06-3.808s.012-2.706.058-3.71c.046-1.003.2-1.605.41-2.124a3.397 3.397 0 00-1.21-1.21c-.21-.519-.364-1.121-.41-2.124-.046-1.004-.058-1.348-.058-3.71s.012-2.706.058-3.71c.046-1.003.2-1.605.41-2.124a3.397 3.397 0 00-1.21-1.21c-.519-.21-1.121-.364-2.124-.41-1.004-.046-1.348-.058-3.71-.058s-2.706.012-3.71.058zM12 15.437a3.437 3.437 0 110-6.874 3.437 3.437 0 010 6.874zm0-8.375a4.938 4.938 0 100 9.875 4.938 4.938 0 000-9.875zM16.75 8.25a1.25 1.25 0 11-2.5 0 1.25 1.25 0 012.5 0z"
              clip-rule="evenodd" />
          </svg>
        </a>
        <a href="#" class="text-white hover:text-cinza">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd"
              d="M19.812 5.418c.861.23 1.538.907 1.768 1.768C21.998 8.78 22 12 22 12s0 3.22-.42 4.814c-.23.861-.907 1.538-1.768 1.768C18.22 19 12 19 12 19s-6.22 0-7.812-.42c-.861-.23-1.538-.907-1.768-1.768C2.002 15.22 2 12 2 12s0-3.22.42-4.814c.23-.861.907-1.538 1.768-1.768C5.78 5 12 5 12 5s6.22 0 7.812.418zM9.75 15.5V8.5l6.5 3.5-6.5 3.5z"
              clip-rule="evenodd" />
          </svg>
        </a>
      </div>
      <hr class="border-t-2 border-vermelho my-2" />

      <a @click="toggleDropdown('detran')" href="#"
        class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold flex justify-between items-center">
        Detran
        <svg class="w-5 h-5" :class="{ 'rotate-180': isDetranDropdownOpen }" fill="none" stroke="currentColor"
          viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
        </svg>
      </a>
      <div v-if="isDetranDropdownOpen" class="flex flex-col pl-6">
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Sobre o Detran</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Estrutura</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Diretoria</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Ciretrans</a>
      </div>

      <a @click="toggleDropdown('servicos')" href="#"
        class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold flex justify-between items-center">
        Serviços
        <svg class="w-5 h-5" :class="{ 'rotate-180': isServicosDropdownOpen }" fill="none" stroke="currentColor"
          viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
        </svg>
      </a>
      <div v-if="isServicosDropdownOpen" class="flex flex-col pl-6">
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Habilitação</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Veículos</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Infrações</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Consulta</a>

        <a @click="toggleDropdown('novo')" href="#"
          class="px-4 py-2 hover:bg-white hover:text-vermelho flex justify-between items-center">
          Novo Menu
          <svg class="w-5 h-5" :class="{ 'rotate-180': isNewDropdownOpen }" fill="none" stroke="currentColor"
            viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
          </svg>
        </a>
        <div v-if="isNewDropdownOpen" class="flex flex-col pl-6">
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Item 1</a>
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Item 2</a>
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Item 3</a>
        </div>
      </div>

      <a @click="toggleDropdown('noticias')" href="#"
        class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold flex justify-between items-center">
        Notícias
        <svg class="w-5 h-5" :class="{ 'rotate-180': isNoticiasDropdownOpen }" fill="none" stroke="currentColor"
          viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
        </svg>
      </a>
      <div v-if="isNoticiasDropdownOpen" class="flex flex-col pl-6">
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Últimas Notícias</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Eventos</a>
        <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho">Artigos</a>
      </div>

      <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Educação</a>
      <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Admin./Financeiro</a>
      <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Transparência
        Pública</a>
      <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Estatística</a>
      <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Contato</a>
    </div>
  </div>
  <nav id="nav" class="bg-azul text-white hidden md:block">
    <div class="container mx-auto flex justify-between items-center py-2">
      <div class="flex-1 flex justify-center items-center">
        <div class="flex items-center space-x-4">
          <div class="relative group">
            <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Detran</a>
            <div
              class="absolute left-0 mt-2 w-48 bg-white text-azul shadow-lg z-10 border border-gray-200 hidden group-hover:block transition-all duration-300 opacity-0 group-hover:opacity-100">
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Sobre o Detran</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Estrutura</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Diretoria</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Ciretrans</a>
            </div>
          </div>

          <div class="relative group">
            <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Serviços</a>
            <div
              class="absolute left-0 mt-2 w-48 bg-white text-azul shadow-lg z-10 border border-gray-200 hidden group-hover:block transition-all duration-300 opacity-0 group-hover:opacity-100">
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Habilitação</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Veículos</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Infrações</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Consulta</a>
              <div class="relative group">
                <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Novo Menu</a>
                <div
                  class="absolute left-full top-0 mt-0 w-48 bg-white text-azul shadow-lg z-20 border border-gray-200 hidden group-hover:block transition-all duration-300 opacity-0 group-hover:opacity-100">
                  <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Item 1</a>
                  <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Item 2</a>
                  <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Item 3</a>
                </div>
              </div>
            </div>
          </div>
          <div class="relative group">
            <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Notícias</a>
            <div
              class="absolute left-0 mt-2 w-48 bg-white text-azul shadow-lg z-10 border border-gray-200 hidden group-hover:block transition-all duration-300 opacity-0 group-hover:opacity-100">
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Últimas Notícias</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Eventos</a>
              <a href="#" class="block px-4 py-2 hover:bg-gray-200 transition-colors duration-200">Artigos</a>
            </div>
          </div>
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Educação</a>
          <a href="#"
            class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Admin./Financeiro</a>
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Transparência
            Pública</a>
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Estatística</a>
          <a href="#" class="px-4 py-2 hover:bg-white hover:text-vermelho fonte-principal font-bold">Contato</a>
        </div>
      </div>
      <div class="flex items-center space-x-2">
        <a href="#" class="text-white hover:text-vermelho">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd"
              d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
              clip-rule="evenodd" />
          </svg>
        </a>
        <a href="#" class="text-white hover:text-vermelho">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.71v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" />
          </svg>
        </a>
        <a href="#" class="text-white hover:text-vermelho">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd"
              d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.024.06 1.378.06 3.808s-.012 2.784-.06 3.808c-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.024.048-1.378.06-3.808.06s-2.784-.013-3.808-.06c-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.048-1.024-.06-1.378-.06-3.808s.012-2.706.058-3.71c.046-1.003.2-1.605.41-2.124a3.397 3.397 0 00-1.21-1.21c-.21-.519-.364-1.121-.41-2.124-.046-1.004-.058-1.348-.058-3.71s.012-2.706.058-3.71c.046-1.003.2-1.605.41-2.124a3.397 3.397 0 00-1.21-1.21c-.519-.21-1.121-.364-2.124-.41-1.004-.046-1.348-.058-3.71-.058s-2.706.012-3.71.058zM12 15.437a3.437 3.437 0 110-6.874 3.437 3.437 0 010 6.874zm0-8.375a4.938 4.938 0 100 9.875 4.938 4.938 0 000-9.875zM16.75 8.25a1.25 1.25 0 11-2.5 0 1.25 1.25 0 012.5 0z"
              clip-rule="evenodd" />
          </svg>
        </a>
        <a href="#" class="text-white hover:text-vermelho">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd"
              d="M19.812 5.418c.861.23 1.538.907 1.768 1.768C21.998 8.78 22 12 22 12s0 3.22-.42 4.814c-.23.861-.907 1.538-1.768 1.768C18.22 19 12 19 12 19s-6.22 0-7.812-.42c-.861-.23-1.538-.907-1.768-1.768C2.002 15.22 2 12 2 12s0-3.22.42-4.814c.23-.861.907-1.538 1.768-1.768C5.78 5 12 5 12 5s6.22 0 7.812.418zM9.75 15.5V8.5l6.5 3.5-6.5 3.5z"
              clip-rule="evenodd" />
          </svg>
        </a>
      </div>
    </div>
  </nav>

  <hr class="border-vermelho mb-8" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import governopara from '../../assets/images/GovernoPara.png';
import logodetran from '../../assets/images/Logodetran.png'

const isMobileMenuOpen = ref(false);
const isDetranDropdownOpen = ref(false);
const isServicosDropdownOpen = ref(false);
const isNoticiasDropdownOpen = ref(false);
const isNewDropdownOpen = ref(false); // Nova variável para o submenu

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const toggleDropdown = (dropdown: string) => {
  // Fecha todos os dropdowns primeiro, a menos que o mesmo seja clicado novamente
  if (dropdown === 'detran') {
    isDetranDropdownOpen.value = !isDetranDropdownOpen.value;
    isServicosDropdownOpen.value = false;
    isNoticiasDropdownOpen.value = false;
    isNewDropdownOpen.value = false; // Garante que o submenu também seja fechado
  } else if (dropdown === 'servicos') {
    isServicosDropdownOpen.value = !isServicosDropdownOpen.value;
    isDetranDropdownOpen.value = false;
    isNoticiasDropdownOpen.value = false;
    isNewDropdownOpen.value = false; // Garante que o submenu também seja fechado
  } else if (dropdown === 'noticias') {
    isNoticiasDropdownOpen.value = !isNoticiasDropdownOpen.value;
    isDetranDropdownOpen.value = false;
    isServicosDropdownOpen.value = false;
    isNewDropdownOpen.value = false; // Garante que o submenu também seja fechado
  } else if (dropdown === 'novo') {
    isNewDropdownOpen.value = !isNewDropdownOpen.value;
  }
};
</script>