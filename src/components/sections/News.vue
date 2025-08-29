<template>
  <div class="bg-gray-50 py-12 mt-12">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-8">
        <div class="mb-4 md:mb-0">
          <h2 class="text-3xl font-bold fonte-principal text-vermelho">Últimas Notícias</h2>
          <p class="text-gray-600 mt-1">Fique por dentro das novidades do DETRAN PA.</p>
        </div>
        <a href="#" class="hidden md:flex bg-white fonte-principal text-azul font-semibold items-center w-fit border border-gray-300 rounded-lg px-4 py-2 transition-colors duration-200 hover:bg-azul hover:text-white">
          Ver Todas
          <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1 transition-transform transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
          </svg>
        </a>
      </div>

      <div class="flex flex-col gap-8">
        <div class="flex md:hidden">
          <a href="#" class="bg-white fonte-principal text-azul font-semibold flex items-center w-full justify-center border border-gray-300 rounded-lg px-4 py-2 transition-colors duration-200 hover:bg-azul hover:text-white">
            Ver Todas
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1 transition-transform transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </a>
        </div>
        
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
          <NewsCard
            v-for="news in newsList"
            :key="news.title"
            :image="news.image"
            :tag="news.tag"
            :date="news.date"
            :title="news.title"
            :description="news.description"
            :link="news.link"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import NewsCard from '../ui/NewsCard.vue'
import post1 from '../../assets/images/post1.jpg'
import post2 from '../../assets/images/post2.jpg'
import post3 from '../../assets/images/post3.jpg'

interface News {
  image: string;
  tag: string;
  date: string;
  title: string;
  description: string;
  link: string;
}

export default defineComponent({
  name: 'News',
  components: {
    NewsCard,
  },
  setup() {
    const newsList = ref<News[]>([
      {
        image: post1 ,
        tag: 'Tecnologia',
        date: '14/03/2024',
        title: 'DETRAN PA inaugura novo sistema de atendimento digital',
        description: 'Sistema permite agendamento online e reduz filas nos postos de atendimento.',
        link: '#',
      },
      {
        image: post2,
        tag: 'Documentos',
        date: '09/03/2024',
        title: 'CNH Digital agora disponível para todos os condutores paraenses',
        description: 'Documento eletrônico tem a mesma validade da versão impressa e oferece mais praticidade.',
        link: '#',
      },
      {
        image: post3,
        tag: 'Educação',
        date: '04/03/2024',
        title: 'Campanha de educação no trânsito percorre interior do Pará',
        description: 'Ações educativas visam reduzir acidentes e promover a cultura de segurança viária.',
        link: '#',
      },
    ]);

    return {
      newsList,
    };
  },
});
</script>