<template>
  <div class="show-props messenger__prop-btn">
    <PropertiesBtn className="show-props__btn" @click="handlePropsClick" />
    <ul v-if="propsIsShown" class="show-props__props-list">
      <li @click="handlePropClick" class="show-props__props-item">Обратная связь о работе сервиса</li>
      <li @click="handlePropClick" class="show-props__props-item">Сменить помощника</li>
    </ul>
  </div>
</template>

<script>
import { PropertiesBtn } from '../../../../shared/ui/buttons/PropertiesBtn';

export default {
  name: 'ShowProps',
  data() {
    return {
      propsIsShown: false,
    };
  },
  props: {
    className: String,
  },
  components: { PropertiesBtn },
  methods: {
    handlePropsClick() {
      this.propsIsShown = true;
    },
    handlePropClick() {
      this.propsIsShown = false;
    },
  },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
