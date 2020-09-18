<template>
  <div class="card">
    <span>
      <div class="relative">
        <div class="glide glide--ltr glide--slider glide-swipeable">
          <div data-glide-el="track" class="glide__track">
            <ul class="glide__slides" style="transition: transform 0ms cubic-bezier(0.165, 0.84, 0.44, 1) 0s; width: 1440px; transform: translate3d(0px, 0px, 0px);">
              <li data-glide-index="0" class="glide__slide glide__slide--active" style="width: 288px; margin-right: 0px">
                <!-- <div class="stamp">
                  <img src="https://image.casafy.com/site/v1.1/gold.svg" class="symbol">
                  <p class="gold">100% verificado</p>
                </div> -->
                <nuxt-link to="#">
                  <img class="images" v-bind:src=" imgUrl (imovel.main_picture) ">
                </nuxt-link>
              </li>
              <!-- <li data-glide-index="0" class="glide__slide glide__slide--active" style="width: 288px; margin-right: 0px">
                <div class="stamp">
                  <img src="https://image.casafy.com/site/v1.1/gold.svg" class="symbol">
                  <p class="gold">100% verificado</p>
                </div>
                <nuxt-link to="#">
                  <img class="images" v-bind:src=" imgUrl (imovel.pictures) ">
                </nuxt-link>
              </li> -->
            </ul>
          </div>
          <!-- <div class="controls">
            <div data-glide-dir="<" class="glide-control-prev"></div>
            <div data-glide-dir=">" class="glide-control-next"></div>
          </div> -->
        </div>
        <h5 class="absolute bottom-0 right-0 mr-3 mb-3">
          <span class="green-badge text-custom-xxs">COMPRE</span>
        </h5>
      </div>
      </span>
      <div class="p-3">
        <div class="border-b pb-3">
          <div class="flex flex-wrap items-center">
            <h5 class="w-3/5 text-base text-gray-700 font-bold leading-none">R$&nbsp;{{ imovel.price }}</h5>
            <h5 class="w-2/5valid text-right">Direto com o proprietário</h5>
            <br>
          </div>
          <p class="text-xs text-red-500 font-semibold uppercase leading-none">{{ imovel.property_type }}</p>
          <p class="text-base text-gray 600 font-semibold mb-2">
            <span>{{ imovel.neighborhood }} - {{ imovel.city }} - {{ imovel.state }}</span>
          </p>
          <div class="flex items-center text-sm text-gray-600 font-light italic">
            <span aria-label="Map Marker icon" role="img" class="material-design-icon map-marker-icon text-4xl">
              <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24" class="material-design-icon__svg">
                <path d="M12,11.5A2.5,2.5 0 0,1 9.5,9A2.5,2.5 0 0,1 12,6.5A2.5,2.5 0 0,1 14.5,9A2.5,2.5 0 0,1 12,11.5M12,2A7,7 0 0,0 5,9C5,14.25 12,22 12,22C12,22 19,14.25 19,9A7,7 0 0,0 12,2Z">
                  <title>Map Marker icon</title>
                </path>
              </svg>
            </span>
          </div>
        </div>
      </div>
      <div class="flex flex-row justify-start items-center px-3 pb-3">
        <p class="flex items-center text-sm text-gray-600 font-light mr-4">
          <span aria-label="Home icon" role="img" class="material-design-icon home-icon text-3xl mr-1">
            <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24"  class="material-design-icon__svg">
              <path d="M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z">
                <title>Home icon</title>
              </path>
            </svg>
          </span>
          {{ imovel.total_area }}m²
        </p>
        <p class="flex items-center text-sm text-gray-600 font-light">
          <span aria-label="Hotel icon" role="img" class="material-design-icon home-icon text-3xl mr-1">
            <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24"  class="material-design-icon__svg">
              <path d="M19,7H11V14H3V5H1V20H3V17H21V20H23V11A4,4 0 0,0 19,7M7,13A3,3 0 0,0 10,10A3,3 0 0,0 7,7A3,3 0 0,0 4,10A3,3 0 0,0 7,13Z">
                <title>Hotel icon</title>
              </path>
            </svg>
          </span>
          {{ imovel.bedrooms }} quartos
        </p>
      </div>
  </div>
</template>

<script>
export default {
  name: 'CardsImoveis',
  props: ['imovel', 'id'],
  methods: {
    imgUrl (img) {
      const newUrl = 'https://imaginary.casafy.com.br/pipeline?operations=[{"operation": "smartcrop", "params":{"width": 320, "height": 192}}]&url=' + img
      return newUrl
    }
  }
}
</script>

<style>
.green-badge{
background-color: rgba(62, 167, 167, 1);
text-transform: uppercase;
padding: .25rem .5rem;
font-size: .75rem;
font-weight: 700;
color: rgba(255, 255, 255, 1);
}
.card{
  max-width: 18rem;
  max-height: 410px;
  height: 100%;
  width: 100%;
  box-shadow: 0 2px 2px rgba(0, 0, 0, .2);
  border-radius: .25rem;
  background-color: rgba(255, 255, 255, 1);
  overflow: hidden;
  cursor: pointer;
}
.stamp{
  position: absolute;
  opacity: .85;
  width: 13rem;
}

.stamp .symbol{
  position: absolute;
  margin-top: .5rem;
  margin-left: .5rem;
  width: 39px;
}
</style>
