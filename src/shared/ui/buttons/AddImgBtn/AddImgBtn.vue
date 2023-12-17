<template>
  <button type="button" class="add-img-btn" :class="className">
    <ImgIcon/>
  </button>
</template>

<script>
import { ImgIcon } from '../../icons';

export default {
  name: 'AddImgBtn',
  props: {
    className: String,
  },
  components: { ImgIcon },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>