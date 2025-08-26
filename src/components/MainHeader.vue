<template>
  <div class="bg-white py-4">
    <div class="container mx-auto flex justify-between items-center px-4">
      <!-- Logo -->
      <div class="flex items-center">
        <div class="w-32 h-16 bg-gray-300 flex items-center justify-center">
          <span class="text-gray-500 text-sm">Logo Placeholder</span>
        </div>
      </div>

      <!-- Social Media and Links -->
      <div class="flex items-center space-x-6">
        <a href="#" class="text-blue-800 font-bold hover:underline">Agência Pará</a>
        <a href="#" class="text-blue-800 font-bold hover:underline">Portal do Servidor</a>
        <div class="flex items-center space-x-2">
          <!-- Social Media Icons -->
          <a href="#" class="text-gray-600 hover:text-blue-800">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path
                fill-rule="evenodd"
                d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
                clip-rule="evenodd"
              />
            </svg>
          </a>
          <a href="#" class="text-gray-600 hover:text-blue-800">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path
                d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.71v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"
              />
            </svg>
          </a>
          <a href="#" class="text-gray-600 hover:text-blue-800">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path
                fill-rule="evenodd"
                d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.024.06 1.378.06 3.808s-.012 2.784-.06 3.808c-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.024.048-1.378.06-3.808.06s-2.784-.013-3.808-.06c-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.048-1.024-.06-1.378-.06-3.808s.012-2.784.06-3.808c.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 016.08 2.525c.636-.247 1.363-.416 2.427-.465C9.53 2.013 9.884 2 12.315 2zm-1.161 1.545c-1.003.046-1.605.2-2.124.41a3.397 3.397 0 00-1.21 1.21c-.21.519-.364 1.121-.41 2.124-.046 1.004-.058 1.348-.058 3.71s.012 2.706.058 3.71c.046 1.003.2 1.605.41 2.124a3.397 3.397 0 001.21 1.21c.519.21 1.121.364 2.124.41 1.004.046 1.348.058 3.71.058s2.706-.012 3.71-.058c1.003-.046 1.605-.2 2.124-.41a3.397 3.397 0 001.21-1.21c.21-.519.364-1.121.41-2.124.046-1.004.058-1.348.058-3.71s-.012-2.706-.058-3.71c-.046-1.003-.2-1.605-.41-2.124a3.397 3.397 0 00-1.21-1.21c-.519-.21-1.121-.364-2.124-.41-1.004-.046-1.348-.058-3.71-.058s-2.706.012-3.71.058zM12 15.437a3.437 3.437 0 110-6.874 3.437 3.437 0 010 6.874zm0-8.375a4.938 4.938 0 100 9.875 4.938 4.938 0 000-9.875zM16.75 8.25a1.25 1.25 0 11-2.5 0 1.25 1.25 0 012.5 0z"
                clip-rule="evenodd"
              />
            </svg>
          </a>
          <a href="#" class="text-gray-600 hover:text-blue-800">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path
                fill-rule="evenodd"
                d="M19.812 5.418c.861.23 1.538.907 1.768 1.768C21.998 8.78 22 12 22 12s0 3.22-.42 4.814c-.23.861-.907 1.538-1.768 1.768C18.22 19 12 19 12 19s-6.22 0-7.812-.42c-.861-.23-1.538-.907-1.768-1.768C2.002 15.22 2 12 2 12s0-3.22.42-4.814c.23-.861.907-1.538 1.768-1.768C5.78 5 12 5 12 5s6.22 0 7.812.418zM9.75 15.5V8.5l6.5 3.5-6.5 3.5z"
                clip-rule="evenodd"
              />
            </svg>
          </a>
        </div>
      </div>
    </div>
    <!-- Main Navigation -->
    <nav id="nav" class="bg-blue-800 text-white mt-4">
      <div class="container mx-auto flex justify-left">
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Detran</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Serviços</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Notícias</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Educação</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Admin./Financeiro</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Transparência Pública</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Estatística</a>
        <a href="#" class="px-4 py-2 hover:bg-blue-700">Contato</a>
      </div>
    </nav>
  </div>
</template>

<script setup lang="ts">
// No script needed for this simple component
</script>
