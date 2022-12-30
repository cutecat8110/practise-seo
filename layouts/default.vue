<template lang="pug">
.layout
  header
      NavBar
  main
    slot
  footer Copyright © 2022 天樞資訊. All rights reserved.
</template>

<script setup>
const route = useRoute()

watch(
  () => route.meta,
  () => {
    const title = route.meta.title
      ? `${route.meta.title} | 牛角日本燒肉專門店`
      : '牛角日本燒肉專門店 | 燒肉吃到飽'

    const description = route.meta.description
      ? route.meta.description
      : '牛角為日本規模最大、最知名的國際燒肉品牌，全球展店逾750間。牛角的特色是「以合理的價格提供高品質的肉品」，提供單點&套餐＆任您吃等多種消費選擇。'

    const keywords = route.meta.keywords
      ? route.meta.keywords
      : '燒肉,吃到飽,燒肉吃到飽,牛角,日式炭火燒肉,日本,包廂式,燒肉店,分店資訊,菜單,最新消息,啤酒'

    useHead({
      title,
      meta: [
        {
          /* 網頁標題 */
          name: 'title',
          content: title
        },
        {
          /* 內容語言 */
          'http-equiv': 'content-language',
          content: 'zh-TW'
        },
        {
          name: 'author',
          content: '天樞資訊科技有限公司'
        },
        {
          name: 'copyright',
          content: `Copyright © 2022 天樞資訊. All rights reserved.`
        },
        {
          /* 網頁描述 */
          name: 'description',
          content: description
        },
        {
          /* 網頁類型 */
          name: 'keywords',
          content: keywords
        },
        {
          /* 爬蟲下次回訪時間 */
          name: 'revisit-after',
          content: '1 days'
        },
        {
          /* 允許爬蟲搜尋網頁 允許追蹤連結 */
          name: 'robots',
          content: 'index, follow'
        },
        {
          /* 支援流動裝置 */
          name: 'viewport',
          content: 'width=device-width, initial-scale=1'
        },
        {
          name: 'og:type',
          content: 'website'
        },
        {
          name: 'og:locale',
          content: 'tw'
        },
        {
          name: 'og:title',
          content: title
        },
        {
          name: 'og:description',
          content: description
        },
        {
          name: 'og:url',
          content: ''
        },
        {
          name: 'og:site_name',
          content: '牛角日本燒肉專門店|燒肉吃到飽'
        },
        {
          name: 'og:image',
          content: ''
        }
      ]
    })
  },
  { immediate: true }
)
</script>

<style lang="sass" scoped>
.layout
  display: flex
  flex-direction: column
  min-height: 100vh

  main
    flex: 1
</style>
