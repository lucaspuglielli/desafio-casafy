<template>
  <div>
    <FiltroMobile />
    <div class="lg:flex">
      <div class="lg:w-1/2">
      <div class="cards bg-white">
        <div class="lg:relative lg:top-0 lg:z-20">
          <div class="hidden lg:flex justify-between items-center relative bg-gray-100 h-12 px-2 pl-16">
            <div>
              <h1 id="total-properties" class="search-total-items text-sm text-gray-500 ml-10">
                <span class="font-semibold">&nbsp;0</span>
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
              <span class="font-semibold">&nbsp;0</span>
              imóveis
            </h1>
            <button class="relative justify-center items-center w-12 h-12 z-20 bg-teal-500 text-white hidden lg:flex">
              <span aria-label="Format List Bulleted Square icon" role="img" class="material-design-icon format-list-bulleted-square-icon text-5xl">
                <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24" class="material-design-icon__svg">
                  <path d="M3,4H7V8H3V4M9,5V7H21V5H9M3,10H7V14H3V10M9,11V13H21V11H9M3,16H7V20H3V16M9,17V19H21V17H9">
                    <title>Format List Bulleted Square icon</title>
                  </path>
                </svg>
              </span>
            </button>
          </div>
        </div>
        <div id="card-content" class="pt-6 lg:overflow-y-auto lg:overflow-x-visible map-content">
          <div class="flex flex-wrap justify-center"></div>
        </div>
      </div>
      <div class="filter close">
        <div class="lg:realtive lg:top-0 lg:z-30">
          <button id="search-adv-button" class="btn-close-filter flex-justify-center items-center">
            <strong>Filtrar</strong>
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
import FiltroMobile from '../components/FiltroMobile'
import FiltroBox from '../components/FiltroBox'
export default {
  head () {
    return {
      title: 'Casafy. O imóvel dos seus sonhos a apenas alguns cliques de você.'
    }
  },
  name: 'Home',
  components: {
    FiltroMobile,
    FiltroBox
  }
}
</script>

<style>
.cards{
  z-index: 20;
  height: 100%;
}
</style>
