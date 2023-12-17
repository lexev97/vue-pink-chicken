<template>
  <div class="dialog" :class="className">
    <p class="dialog__timestamp">Сегодня, 20:43</p>
    <ManagerMessage />
    <UserMessage />
    <br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
    <br />
  </div>
</template>

<script>
import { ManagerMessage } from '../../../../entities/Messenger/ManagerMessage';
import { UserMessage } from '../../../../entities/Messenger/UserMessage';

export default {
  name: 'ShowMessages',
  props: {
    className: String,
  },
  components: { ManagerMessage, UserMessage },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
