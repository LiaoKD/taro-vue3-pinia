<template>
  <basic-layout>
    <custom-nav-bar title="我是packageB" left-show />
    <div>我是packageB</div>
  </basic-layout>
</template>
<script setup lang="ts">
import { fetchDemo } from '@/service';

definePageConfig({
  navigationBarTitleText: 'packageB',
  enablePullDownRefresh: true,
  backgroundTextStyle: 'dark'
});

async function getDemo() {
  const res = await fetchDemo({ phone: 1 });
  window.console.log(res);
}
getDemo();
</script>

<style lang="scss"></style>
