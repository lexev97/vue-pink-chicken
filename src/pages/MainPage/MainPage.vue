<template>
  <TheHeader />
  <TheBody />
  <TheFooter />
</template>

<script>
import { TheHeader, TheBody, TheFooter } from '@/widgets';

export default {
  name: 'MainPage',
  components: { TheHeader, TheBody, TheFooter },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
