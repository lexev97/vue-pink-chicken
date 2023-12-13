<template>
  <MainPage msg="Welcome to Your Vue.js App" />
</template>

<script>
import './styles/index.scss';

import { MainPage } from '../pages';

export default {
  name: 'App',
  components: {
    MainPage,
  },
};
</script>
