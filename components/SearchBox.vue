<template>
  <div class="w-full relative">
    <input type="text" tabindex="0" placeholder="Em qual bairro ou cidade?" class="form-control address" />
    <ul class="suggestions" style="display:none;"></ul>
    <p style="display:none;">false</p>
  </div>
</template>

<script>
export default {
  name: 'SearchBox'
}
</script>

<style scoped>
.form-control{
width: 25rem;
box-sizing: border-box;
background-color: #f2f2f2;
padding: .6rem;
border: 1px solid #707070;
border-radius: 0.25rem 0 0 0.25rem;
line-height: .8rem;
font-size: 17px;
}
.form-control:focus{
outline: none;
}
</style>
