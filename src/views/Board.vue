<template>
    <div class="board">
        <div class="columns">
            <div class="column"
                v-for="(column, $columnIndex) of board.columns"
                :key="$columnIndex">
                <div class="column-name">
                    {{ column.name }}
                </div>
                <div class="list-reset">
                    <div class="task"
                        v-for="(task, $taskIndex) of column.tasks"
                        :key="$taskIndex">
                        <span class="">
                            {{ task.name }}
                        </span>
                        <p v-if="task.description" class="">
                            {{ task.description }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: mapState(['board'])
}
</script>

<style lang="scss">
.board {
    padding: 15px;
    text-align: left;
    .column {
        div {
            background-color: #dbdbdb;
            padding: 15px;
        }
        font-weight: 600;
        .column-name {
            padding-bottom: 0;
            border-top-left-radius: 5px;
            border-top-right-radius: 5px;
        }
        .list-reset {
            border-bottom-left-radius: 5px;
            border-bottom-right-radius: 5px;
        }
        .task {
            background-color: #fff;
            margin: 0 0 10px;
            border-radius: 5px;
        }
    }
}
</style>
