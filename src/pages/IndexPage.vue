<template>
  <div class="q-pa-md doc-container">
    <div class="row items-start">
      <q-card class="my-card">
        <img
          src="https://logodownload.org/wp-content/uploads/2015/04/whatsapp-logo-png-0.png"
        />

        <q-card-section>
          <div class="text-h6;">Whatsapp</div>
          <div class="text-subtitle2">by Arthur Pinheiro</div>
        </q-card-section>
      </q-card>
    </div>

    <q-badge>items-center</q-badge>
    <div class="row items-center">
      <div class="col">One of three cols</div>
      <div class="col">One of three cols</div>
      <div class="col">One of three cols</div>
    </div>

    <q-badge>items-end</q-badge>
    <div class="row items-end">
      <div class="col">One of three cols</div>
      <div class="col">One of three cols</div>
      <div class="col">One of three cols</div>
    </div>

    <q-badge>self-*</q-badge>
    <div class="row">
      <div class="col self-start">.self-start</div>
      <div class="col self-center">.self-center</div>
      <div class="col self-end">.self-end</div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {
      lorem: ".",
    };
  },
};
</script>

<style lang="sass" scoped>
.my-card
  color:$dark
  width: 100%
  max-width: 250px
</style>
