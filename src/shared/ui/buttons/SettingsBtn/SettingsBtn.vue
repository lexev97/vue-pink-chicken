<template>
  <button type="button" class="setting-btn" :class="className">
    <GearIcon />
  </button>
</template>

<script>
import { GearIcon } from '@/shared/ui/icons';

export default {
  name: 'SettingsBtn',
  props: {
    className: String,
  },
  components: { GearIcon },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
