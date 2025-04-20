<!-- filepath: /home/yorokan2/webpage/topping2/topping/src/pages/IndexPage.vue -->
<template>
  <div>
    <h1 class = "roulette-title">トッピングルーレット</h1>
    <div class = "roulette-explain">ルーレットを回してトッピングを決めよう！
      <RouletteComponent />
    </div>
  </div>
</template>

<script lang="ts">
import RouletteComponent from 'src/components/RouletteComponent.vue';

export default {
  name: 'IndexPage',
  components: {
    RouletteComponent,
  },
}
</script>
