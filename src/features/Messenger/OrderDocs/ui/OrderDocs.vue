<template>
  <div class="order-docs" :class="className">
    <button type="button" class="order-docs__mediaplan" @click="showDocs">Заказать медиаплан</button>
    <button type="button" class="order-docs__report" @click="showDocs">Заказать отчет</button>
  </div>
</template>

<script>
export default {
  name: 'OrderDocs',
  props: {
    className: String,
  },
  methods: {
    showDocs() {
      this.$emit('handle-show-docs-click');
    },
  },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
