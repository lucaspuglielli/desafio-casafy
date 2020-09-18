<template>
  <header class="header-main lg:fixed">
    <div class="flex flex-wrap lg:flex-no-wrap justify-between items-center">
      <div class="flex justify-between items-center w-1/3">
        <div>
          <nuxt-link to="#" class="no-underline nuxt-link-active">
            <img src="https://s3-sa-east-1.amazonaws.com/casafy.static/site/v1.1/fiqueemcasa.png" alt="Casafy" class="hidden lg:block lg:h-10 lg:w-auto">
            <img src="https://s3-sa-east-1.amazonaws.com/casafy.static/site/v1.1/fiqueemcasa.png" alt="Casafy" class="h-8 w-auto lg:hidden">
          </nuxt-link>
        </div>
        <div id="result-search-input" class="w-3/5 right-26 hidden md:block">
          <SearchForm />
        </div>
      </div>
      <div class="flex justify-between items-center w-2/3 md:w3/5">
        <div class="flex justify-end w-5/6 lg:hidden">
          <nuxt-link to="#" class="red-border-btn">Anuncie seu imóvel</nuxt-link>
        </div>
        <div class="block lg:hidden">
          <button class="flex items-center pl-3 py-2 text-gray-600">
            <svg viewbox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" class="fill-current h-6 w-6">
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
            </svg>
          </button>
        </div>
        <div class="z-0 w-full inset-x-0 opacity-90 lg:block hidden text-gray-600">
          <nav class="text-base md:text-sm font-normal md:font-semibold">
            <ul class="lg:flex lg:justify-end items-center">
              <li class="bg-red-200 py-4 lg:hidden flex">
                <div class="pt-1 login">
                  <p class="no-underline block ml-4">Bem-vindo a Casafy</p>
                  <nuxt-link to="#" class="uppercase no-underline ml-4 tracking-wide text-xxs">Entrar</nuxt-link>
                  <nuxt-link to="#" class="uppercase no-underline tracking-wide text-xxs">Cadastre-se</nuxt-link>
                </div>
              </li>
              <li class="pt-3 pb-1 lg:pt-0 lg:pb-0">
                <nuxt-link to="#" class="uppercase no-underline ml-4">Sobre Casafy</nuxt-link>
              </li>
              <li id="blog" class="pb-1 lg:pb-0">
                <nuxt-link title="Blog" to="#" class="uppercase no-underline ml-4" target="blank">Blog</nuxt-link>
              </li>
              <li id="ajuda" class="pb-3 lg:pb-0">
                <nuxt-link title="Ajuda" to="#" class="uppercase no-underline ml-4" target="_blank">Ajuda</nuxt-link>
              </li>
              <li class="hidden lg:block">
                <nuxt-link to="#" class="red-bg-btn-menu ml-4 bg-red-500 text-white font-semibold">Anuncie seu imóvel</nuxt-link>
              </li>
              <li class="pb-1 lg:pb-0">
                <nuxt-link to="#" class="uppercase no-underline ml-4">Cadastre-se</nuxt-link>
              </li>
              <li class="pb-1 lg:pb-0">
                <nuxt-link to="#" class="uppercase no-underline ml-4 pr-4">Entrar</nuxt-link>
              </li>
              <li class="hidden lg:block pt-1">
                <div class="dropdown"></div>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import SearchForm from '../components/SearchForm'
export default {
  name: 'AppHeader',
  components: {
    SearchForm
  }
}
</script>

<style>
header {
  display: block;
}
.header-main {
top: 0;
right: 0;
left: 0;
box-sizing: border-box;
box-shadow: 0 3px 6px rgba(0,0,0,.16078);
padding: .15rem .05rem .15rem .75rem;
z-index: 50;
}
.red-border-btn{
  font-size: .6875rem;
  color: rgba(252, 99, 96, 1);
  padding-right: .15rem .5rem;
  border-color: rgba(252, 99, 96, 1);
}
.red-bg-btn-menu{
  padding: .25rem .5rem;
  border-radius: .25rem;
  text-transform: uppercase;
}
</style>
