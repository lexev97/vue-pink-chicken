<template>
  <button type="button" class="logout-btn" :class="className">
    <LogoutIcon />
  </button>
</template>

<script>
import { LogoutIcon } from '../../icons';

export default {
  name: 'LogoutBtn',
  props: {
    className: String,
  },
  components: { LogoutIcon },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
