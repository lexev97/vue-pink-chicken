<template>
  <button type="button" class="properties-btn" :class="className">
    <DotsIcon />
  </button>
</template>

<script>
import { DotsIcon } from '@/shared/ui/icons';

export default {
  name: 'PropertiesBtn',
  props: {
    className: String,
  },
  components: { DotsIcon },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
