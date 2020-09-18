<template>
  <div class="filtro-mobile">
      <div class="px-2 md:hidden">
        <SearchForm />
      </div>
      <div class="flex justify-start items-center h-10 overflow-x-auto overflow-y-hidden">
        <button class="flex justify-center items-center text-sm text-teal-500 font-semibold uppercase border border-teal-500 rounded py-1 px-2 mx-2">
          <span aria-label="Filter Outline icon" role="img" class="material-design-icon filter-outline-icon text-xl mr-1">
           <svg fill="currentColor" width="24" height="24" viewBox="0 0 24 24" class="material-design-icon__svg">
              <path d="M15,19.88C15.04,20.18 14.94,20.5 14.71,20.71C14.32,21.1 13.69,21.1 13.3,20.71L9.29,16.7C9.06,16.47 8.96,16.16 9,15.87V10.75L4.21,4.62C3.87,4.19 3.95,3.56 4.38,3.22C4.57,3.08 4.78,3 5,3V3H19V3C19.22,3 19.43,3.08 19.62,3.22C20.05,3.56 20.13,4.19 19.79,4.62L15,10.75V19.88M7.04,5L11,10.06V15.58L13,17.58V10.05L16.96,5H7.04Z">
                <title>Filter Outline icon</title>
              </path>
            </svg>
          </span>
        Filtros
        </button>
      </div>
  </div>
</template>

<script>
import SearchForm from '../components/SearchForm'
export default {
  name: 'FiltroMobile',
  components: {
    SearchForm
  }
}
</script>

<style>
@media (min-width: 1024px){
    .filtro-mobile{
        display: none;
    }
}
@media (min-width: 768px){
    .filtro-mobile{
        position: static;
        margin-top: 3rem;
    }
}
.filtro-mobile, .filter{
    top: 0;
    margin-top: 3rem;
    background-color: rgba(242, 242, 242, 1);
}
.filtro-mobile{
    position: -webkit-sticky;
    position: sticky;
    z-index: 30;
    box-shadow: 0 1px 1px rgba(0, 0, 0, .14118);
}
</style>
