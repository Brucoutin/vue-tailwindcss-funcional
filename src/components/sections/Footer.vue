<template>
  <footer class="bg-cinza  text-gray-200 py-10 mt-30" >
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
        <div>
          <div class="flex justify-center mb-4">
            <img src="../../assets/images/logo_detran_min.png" alt="Logo DETRAN PA" class="w-80" />
          </div>
       <!--  <h4 class="font-bold text-lg mb-4">DETRAN PA</h4> -->  
          <p class="text-sm">
            Departamento de Trânsito do Estado do Pará
          </p>
          <p>
             ROD AUGUSTO MONTENEGRO KM/03 S/N
          </p>
          <p>
           BAIRRO: NOVA MARAMBAIA 
          </p>
          <p>
            CEP: 66.630-505
          </p>
          <p>
             CNPJ: 04.822.060/0001-40
          </p>
        </div>

        <div>
          <h4 class="font-bold text-lg text-vermelho mb-4">Serviços</h4>
          <ul class="space-y-2 text-sm">
            <li v-for="link in services" :key="link.text">
              <a :href="link.url" class="hover:underline">{{ link.text }}</a>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold text-lg text-vermelho mb-4">Informações</h4>
          <ul class="space-y-2 text-sm">
            <li v-for="link in info" :key="link.text">
              <a :href="link.url" class="hover:underline">{{ link.text }}</a>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold text-lg text-vermelho mb-4">Contato</h4>
          <div class="space-y-2 text-sm">
            <p>ATENDIMENTO AO PÚBLICO DAS 9H ÀS 15H DE SEGUNDA A SEXTA</p>
            <p>ATENDIMENTO 154 POR TELEFONE</p>
            <p>Ouvidoria: 0800-123-4567</p>
            <p>Email: atendimento@detran.pa.gov.br</p>
            <p>Horário: 8h às 17h</p>
          </div>
        </div>
      </div>

      <hr class="border-vermelho mb-8" />

      <div class="text-center text-sm">
        <p>© 2025 DETRAN PA - Todos os direitos reservados</p>
        <p>Desenvolvido pelo Governo do Estado do Pará</p>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent, type PropType } from 'vue';
import logo_detran_min from '../assets/images/logo_detran_min.png';
interface Link {
  text: string;
  url: string;
}

export default defineComponent({
  name: 'Footer',
  props: {
    services: {
      type: Array as PropType<Link[]>,
      default: () => [
        { text: 'CNH', url: '#' },
        { text: 'Veículos', url: '#' },
        { text: 'Multas', url: '#' },
        { text: 'Todos os Serviços', url: '#' },
      ],
    },
    info: {
      type: Array as PropType<Link[]>,
      required: true,
      default: () => [
        { text: 'Notícias', url: '#' },
        { text: 'Contato', url: '#' },
        { text: 'Transparência', url: '#' },
        { text: 'Lei de Acesso', url: '#' },
      ],
    },
  },
});
</script>