<template>
  <div class="item">
    <span class="item_icon">
      <slot name="icon"></slot>
    </span>
    <h4 class="item_title">
      <slot name="title"></slot>
    </h4>
    <p class="item_detail">
      <slot name="detail"></slot>
    </p>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
.item
  min-width: 289px !important
  max-width: 290px !important
  height: 428px
  padding: 46px 23px
  background-color: #fff
  border: 1px solid #ececf2
  margin-right: 35px
  font-size: 10px
  position: relative
  color: $primary
  &_title
    font-size: 2.2em
    margin-top: 3.3*10px
    margin-bottom: 2.2*10px
  &_detail
    font-size: 1.6em
  &:before
    z-index: -1
    overflow: hidden
    content: ''
    position: absolute
    border: 1px solid #ececf2
    right: -19px
    bottom: -19px
    width: 100%
    height: 100%
    transition: ease 0.5s all
    border-top: 0
    border-left: 0
  &:hover
    border: 1px solid $primary
    &:before
      border: 16px solid $primary
      border-top: 0
      border-left: 0
      right: -16px
      bottom: -16px
</style>
