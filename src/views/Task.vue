<template>
    <div class="task-view">
        <div class="task-modal">
            {{ task.name }}
        </div>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters([
      'getTask'
    ]),
    task () {
      return this.getTask(this.$route.params.id)
    }
  }
}
</script>

<style lang="scss" scoped>
    .task-modal {
        background-color: #fff;
        padding: 15px;
        border-radius: 5px;
        width: 50%;
    }
</style>
