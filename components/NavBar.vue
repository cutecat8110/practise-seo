<template lang="pug">
nav(class="navbar")
  NuxtLink(to="/about") 牛角簡介
  NuxtLink(to="/menu") 消費介紹
  NuxtLink(to="/store") 分店・訂位資訊
  NuxtLink(to="/" class="home") ✿
  NuxtLink(to="/news") 最新消息
  NuxtLink(to="/contact") 聯絡我們
  NuxtLink(to="/shop") 線上購物
</template>

<script setup></script>

<style lang="sass" scoped>
.navbar
  display: flex
  align-items: center
  justify-content: center
  gap: 1.5rem
  height: 3.5rem
  box-shadow: 0 0 4px rgba(0, 0, 0, 0.2)

  a
    text-decoration: none
    font-weight: 700
    font-size: 0.875rem
    letter-spacing: 0.1em
    color: #212529
    transition: color 0.1s ease-in-out

    &:hover
      color: #42A5F5

    &:active
      color: #1565C0

    &.home
      font-size: 1.5rem

    &.router-link-active
      color: #EF476F
</style>
