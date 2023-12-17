<template>
  <button type="button" class="add-img-btn" :class="className">
    <FolderIcon />
  </button>
</template>

<script>
import { FolderIcon } from '../../icons';

export default {
  name: 'AddImgBtn',
  props: {
    className: String,
  },
  components: { FolderIcon },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
