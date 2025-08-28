<template>
  <div class="p-8 mt-[20px]">
    <h2 class="text-3xl font-bold text-center text-vermelho mb-2">Serviços para Você</h2>
    <p class="text-center text-gray-600 mb-8">
      Acesse os principais serviços do DETRAN PA de forma digital e presencial.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <Card
        v-for="(card, index) in cards"
        :key="index"
        :title="card.title"
        :description="card.description"
        :icon="card.icon"
      >
        <button
           :href="card.url"
              class="w-full border border-gray-300 rounded-lg py-2 flex items-center justify-center gap-2 text-azul hover:bg-azul hover:text-white transition font-bold"
        >
          Acessar Serviço
          <span class="font-bold">→</span>
        </button>
      </Card>
    </div>
  </div>
</template>

<script setup>
import Card from '../ui/Card.vue'
import { faIdCard, faCar, faTriangleExclamation, faDollarSign, faCalendar, faPhone } from '@fortawesome/free-solid-svg-icons'

const cards = [
  {
    title: "CNH",
    description: "Renovação, segunda via e habilitação",
    icon: faIdCard,
    url: "https://www.detran.pa.gov.br/cnh"
  },
  {
    title: "Veículos",
    description: "Licenciamento, transferência e documentos",
    icon: faCar,
    url: "https://www.detran.pa.gov.br/veiculos"
  },
  {
    title: "Multas",
    description: "Consultar e pagar multas de trânsito",
    icon: faTriangleExclamation,
    url: "https://www.detran.pa.gov.br/multas"
  },
  {
    title: "Taxas e Emolumentos",
    description: "Valores atualizados dos serviços",
    icon: faDollarSign,
    url: "https://www.detran.pa.gov.br/taxas"
  },
  {
    title: "Agendamento",
    description: "Agende seu atendimento online",
    icon: faCalendar,
    url: "https://www.detran.pa.gov.br/agendamento"
  },
  {
    title: "Atendimento",
    description: "Central de relacionamento e ouvidoria",
    icon: faPhone,
    url: "https://www.detran.pa.gov.br/atendimento"
  },
]
</script>