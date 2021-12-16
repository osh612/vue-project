<template>
  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>{{product[selection].title}}</h4>
      <div>
        <img :src="product[selection].image">
      </div>
      <p> {{ product[selection].price }}원</p>
      <p>{{product[selection].content}}</p>
      <div>
        <button class="exitmodal" @click="modal = false">
          X
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>