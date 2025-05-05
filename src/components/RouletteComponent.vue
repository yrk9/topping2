<template>
  <div>
    <ul>
      <button @click="onSpinRoulette">ルーレットを回す</button>
    </ul>
    <p v-if="selectedItem">選ばれたトッピング: {{ selectedItem }}</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface RouletteItem {
  id: number;
  content: string;
};

const selectedItem = ref<string | null>(null);

const rouletteItems: RouletteItem[] = [
  { id: 1, content: 'トロ肉' },
  { id: 2, content: 'ブロック肉' },
  { id: 3, content: 'メンマ' },
];

function spinRoulette(): string {
  const randomIndex: number = Math.floor(Math.random() * rouletteItems.length);
  const selectedItem: string = rouletteItems[randomIndex]?.content || 'Default Item';
  
  return selectedItem;
}

function onSpinRoulette() {
  selectedItem.value = spinRoulette();
}
</script>
