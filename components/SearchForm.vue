<template>
  <form>
    <div class="flex">
      <div class="w-full max-w-custom flex flex-wrap relative">
        <SearchBox />
      </div>
    </div>
    <input type="submit" value="Buscar" class="btn-search">
  </form>
</template>

<script>
import SearchBox from '../components/SearchBox'
export default {
  name: 'SearchForm',
  components: {
    SearchBox
  }
}
</script>

<style scoped>
.max-w-custom{
  max-width: 25rem;
}
form{
  display: flex;
}
.btn-search{
  left: -5px;
  z-index: 999!important;
  display: flex;
  justify-content: center;
  align-items: center;
  color: rgba(255,255,255,1);
  font-size: .875rem;
  background-color: rgba(252, 99, 96, 1);
  border-width: 1px;
  border-color: rgba(252, 99, 96, 1);
  padding-left: .75rem;
  padding-right: .75rem;
  border-top-right-radius: .5rem;
  border-bottom-right-radius: .5rem;
  text-transform: uppercase;
  font-weight: 600;
}
</style>
