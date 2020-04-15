<template>
  <agile>
    <div v-for="n in 6" class="slide" :class="'slide--' + n">{{ n }}</div>
  </agile>
</template>

<script>
  export default {
    name: 'Carousel'
  }
</script>

<style lang="sass">
  // Basic VueAgile styles
  .agile
    margin-top: 20px

    &__actions
      margin-top: 20px

    &__nav-button
      background: transparent
      border: none
      color: #ccc
      cursor: pointer
      font-size: 24px
      transition-duration: .3s

      &:hover
        color: #888

    &__dot
      margin: 0 10px

      button
        background-color: #eee
        border: none
        border-radius: 50%
        cursor: pointer
        display: block
        height: 10px
        font-size: 0
        line-height: 0
        margin: 0
        padding: 0
        transition-duration: .3s
        width: 10px

      &--current,
      &:hover
        button
          background-color: #888

  // Slides styles
  .slide
    align-items: center
    color: #fff
    display: flex
    font-size: 32px
    font-weight: 300
    height: 200px
    justify-content: center

  // Slides backgrounds
  $colors: #f1c40f #e67e22 #e74c3c #9b59b6 #3498db #2ecc71

  @for $i from 1 through length($colors)
    $color: nth($colors, $i)

    .slide--#{$i}
      background-color: $color

</style>
