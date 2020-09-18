<template>
  <div>
    <FiltroMobile />
    <div class="lg:flex">
      <div class="lg:w-1/2">
        <div class="cards bg-white">
          <div class="lg:relative lg:top-0 lg:z-20">
            <div class="hidden justify-between items-center relative bg-gray-100 h-12 px-2 pl-16">
              <div>
                <h1 id="total-properties" class="search-total-items text-sm text-gray-500 ml-10">
                  <span class="font-semibold">&nbsp;{{ qtd }}</span>
                  imóveis
                </h1>
              </div>
              <button class="flex justify-center items-center w-12 h-12 z-20 bg-red-500 text-white right-12">
                <span aria-label="Close icon" role="img" class="material-design-icon close-icon text-5xl">
                  <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24" class="material-design-icon__svg">
                    <path d="M19,6.41L17.59,5L12,10.59L6.41,5L5,6.41L10.59,12L5,17.59L6.41,19L12,13.41L17.59,19L19,17.59L13.41,12L19,6.41Z">
                      <title>Close icon</title>
                    </path>
                  </svg>
                </span>
              </button>
            </div>
            <div class="flex justify-between items-center relative-h-12 bg-white shadow px-2 lg:pl-16">
              <h1 class="search-total-items text-sm text-gray-500 ml-12">
                <span class="font-semibold">&nbsp;{{ qtd }}</span>
                imóveis
              </h1>
              <button class="relative justify-center items-center w-12 h-12 z-20 bg-teal-500 text-white hidden lg:flex button-postion-right">
                <span aria-label="Format List Bulleted Square icon" role="img" class="material-design-icon format-list-bulleted-square-icon text-5xl">
                  <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24" class="material-design-icon__svg testetranformers">
                    <path d="M3,4H7V8H3V4M9,5V7H21V5H9M3,10H7V14H3V10M9,11V13H21V11H9M3,16H7V20H3V16M9,17V19H21V17H9">
                      <title>Format List Bulleted Square icon</title>
                    </path>
                  </svg>
                </span>
              </button>
            </div>
          </div>
          <div id="card-content" class="pt-6 lg:overflow-y-auto lg:overflow-x-visible map-content">
            <div class="flex flex-wrap justify-evenly">
              <CardsImoveis v-for="imovel in imoveis" :id="imovel.id" :key="imovel.id" :imovel="imovel" />
            </div>
          </div>
        </div>
        <div class="filter close">
          <div class="lg:realtive lg:top-0 lg:z-30">
            <button id="search-adv-button" class="btn-close-filter flex-justify-center items-center">
              <strong>FILTRAR</strong>
            </button>
          </div>
          <FiltroBox />
        </div>
      </div>
      <div class="lg:w-1/2"></div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import FiltroMobile from '../components/FiltroMobile'
import FiltroBox from '../components/FiltroBox'
import CardsImoveis from '../components/CardsImoveis'
export default {
  name: 'Home',
  components: {
    FiltroMobile,
    FiltroBox,
    CardsImoveis
  },
  methods: {

  },
  data () {
    return {
      imoveis: [],
      qtd: 0
    }
  },
  async created () {
    try {
      const res = await axios.get('https://api.homol.casafy.com.br/search?url=sp/sao-paulo/venda-direta')
      this.imoveis = res.data.results
      this.qtd = this.imoveis.length
      console.log(this.imoveis)
    } catch (err) {
      console.log(err)
    }
  },
  head () {
    return {
      title: 'Casafy. O imóvel dos seus sonhos a apenas alguns cliques de você.'
    }
  }
}
</script>

<style>
@import url("node_modules/@glidejs/glide/dist/css/glide.core.min.css");
.cards{
  z-index: 20;
  height: 100%;
}
.button-postion-right{
  right: -3.65rem;
}
.testetranformers{
  transform: scale(1.7);
}
.filter.close{
  left: -100%;
  position: absolute;
}
.btn-close-filter{
  top: .5rem;
  right: .5rem;
  position: absolute;
  z-index: 30;
  height: 2.5rem;
  background-color: rgba(252, 99 , 96, 1);
  color: rgba(255, 255, 255, 1);
  padding-left: 1.25rem;
  padding-right: 1.25rem;
}
@media (min-width: 1024px) {
  .filter{
    margin-top: 3rem;
  }
  .btn-close-filter{
    top: 3rem;
    right: -6rem;
    display: flex;
    justify-content: center;
    width: 6rem;
    position: absolute;
    height: 3rem;
    z-index: 30;
    background-color: rgba(252, 99, 96, 1);
    color: rgba(255, 255, 255, 1);
  }
}
  @media (min-width: 768px) {
  .filter{
    margin-top: 0;
  }
}
.filter{
  width: 100%;
  top: 0;
  background-color: rgba(242, 242, 242, 1);
}

</style>
