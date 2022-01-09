<template>
  <div class="q-pa-md q-gutter-md">
    <div>
      <q-btn-toggle
        v-model="model"
        class="my-custom-toggle"
        no-caps
        rounded
        unelevated
        toggle-color="primary"
        color="white"
        text-color="primary"
        :options="[
          {label: 'HOME', value: 'one'}
        ]"
        @click="$router.replace('/')"
      />
    </div>
    <q-card class="my-card">
      <img src="https://images.contentstack.io/v3/assets/bltb6530b271fddd0b1/blt86cd8572a30911aa/60cbfdb00ece0255888d895a/V_Ep_03_REFLECTION_Article-Header.jpg?auto=webp&disable=upscale&height=1055">

      <q-card-section>
        <div class="text-h6">สิ่งที่ฉันชอบทำเวลาว่าง</div>
        <div class="text-subtitle2">นั่งเล่นเกมส์ และฟังเพลง</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <q-img src="https://i.ytimg.com/vi/ua-iIRQDY8g/maxresdefault.jpg">
        <div class="absolute-bottom text-subtitle2 text-center">
          ตัวละครที่ชอบ
        </div>
      </q-img>
    </q-card>
    
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      model: ref('one')
    }
  }
}
</script>

<style lang="sass" scoped>
.my-custom-toggle
  border: 1px solid #027be3
</style>
