<template>
  <div class="page">
    <slot/>

    <!-- <Content :custom="false"/> -->

    <!-- <div class="page-edit"> -->
    <!--   <div -->
    <!--     class="edit-link" -->
    <!--     v-if="editLink" -->
    <!--   > -->
    <!--     <a -->
    <!--       :href="editLink" -->
    <!--       target="_blank" -->
    <!--       rel="noopener noreferrer" -->
    <!--     >{{ editLinkText }}</a> -->
    <!--     <OutboundLink/> -->
    <!--   </div> -->

    <!--   <div -->
    <!--     class="last-updated" -->
    <!--     v-if="lastUpdated" -->
    <!--   > -->
    <!--     <span class="prefix">{{ lastUpdatedText }}: </span> -->
    <!--     <span class="time">{{ lastUpdated }}</span> -->
    <!--   </div> -->
    <!-- </div> -->

    <!-- <div class="page-nav" v-if="prev || next"> -->
    <!--   <p class="inner"> -->
    <!--     <span -->
    <!--       v-if="prev" -->
    <!--       class="prev" -->
    <!--     > -->
    <!--       ← -->
    <!--       <router-link -->
    <!--         v-if="prev" -->
    <!--         class="prev" -->
    <!--         :to="prev.path" -->
    <!--       > -->
    <!--         {{ prev.title || prev.path }} -->
    <!--       </router-link> -->
    <!--     </span> -->

    <!--     <span -->
    <!--       v-if="next" -->
    <!--       class="next" -->
    <!--     > -->
    <!--       <router-link -->
    <!--         v-if="next" -->
    <!--         :to="next.path" -->
    <!--       > -->
    <!--         {{ next.title || next.path }} -->
    <!--       </router-link> -->
    <!--       → -->
    <!--     </span> -->
    <!--   </p> -->
    <!-- </div> -->

    <slot name="bottom"/>
  </div>
</template>

<style lang="stylus">
@import './vuepress/styles/config.styl'
@require './vuepress/styles/wrapper.styl'

.page
  padding-top $navbarHeight
  padding-bottom 2rem

.page-edit
  @extend $wrapper
  padding-top 1rem
  padding-bottom 1rem
  overflow auto
  .edit-link
    display inline-block
    a
      color lighten($textColor, 25%)
      margin-right 0.25rem
  .last-updated
    float right
    font-size 0.9em
    .prefix
      font-weight 500
      color lighten($textColor, 25%)
    .time
      font-weight 400
      color #aaa

.page-nav
  @extend $wrapper
  padding-top 1rem
  padding-bottom 0
  .inner
    min-height 2rem
    margin-top 0
    border-top 1px solid $borderColor
    padding-top 1rem
    overflow auto // clear float
    ul
      padding 0
  .next
    float right

@media (max-width: $MQMobile)
  .page-edit
    .edit-link
      margin-bottom .5rem
    .last-updated
      font-size .8em
      float none
      text-align left

</style>
