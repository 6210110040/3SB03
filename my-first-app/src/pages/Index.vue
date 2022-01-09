<template>
  <div class="q-pa-md q-gutter-md">
    <q-carousel
      arrows
      animated
      v-model="slide"
      height="400px"
    >
      <q-carousel-slide name="first" img-src="https://scontent.fhdy1-1.fna.fbcdn.net/v/t1.6435-1/p240x240/77008180_2463143110672525_2571969559514841088_n.jpg?_nc_cat=106&ccb=1-5&_nc_sid=7206a8&_nc_ohc=xtekeObscDkAX-tIbHq&_nc_ht=scontent.fhdy1-1.fna&oh=00_AT_HR17BtSQVeyOo475bRfBRtPz-t-rRjRJ4kqDw7-uzZg&oe=62016C85">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">First stop</div>
          <div class="text-subtitle1">My Profile</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="second" img-src="https://scontent.fhdy1-1.fna.fbcdn.net/v/t1.6435-9/68751013_2367724860214351_5277194722815770624_n.jpg?_nc_cat=106&ccb=1-5&_nc_sid=174925&_nc_ohc=ynEfx5kWXCYAX9WNXIp&_nc_ht=scontent.fhdy1-1.fna&oh=00_AT8QQNG2u7Hw9HAW8ROUAW94k72sIIEy6VRCC-Pxyk2Zhg&oe=6201C5C1">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">Second stop</div>
          <div class="text-subtitle1">About me</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="third" img-src="https://scontent.fhdy1-1.fna.fbcdn.net/v/t1.6435-9/40203609_2118771275109712_6312911354508345344_n.jpg?_nc_cat=107&ccb=1-5&_nc_sid=174925&_nc_ohc=-dkdPYXjtFQAX924OES&_nc_ht=scontent.fhdy1-1.fna&oh=00_AT-mm4SM72F0aCJjCH7DkdVeCUSiG3g_Xo8eJtvk791ljA&oe=6200F652">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">Third stop</div>
          <div class="text-subtitle1">End credit</div>
        </div>
      </q-carousel-slide>
    </q-carousel>
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
          {label: 'About_Me', value: 'two'}
        ]"
        @click="$router.replace('/aboutme')"
      />
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref('first')
    }
  }
}
</script>

<style lang="sass" scoped>
.custom-caption
  text-align: center
  padding: 12px
  color: white
  background-color: rgba(0, 0, 0, .3)
</style>
