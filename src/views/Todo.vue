<template>
  <div class="home">
    <field-add-task />
    <list-tasks v-if="$store.state.tasks.length"/>
    <no-task v-else/>
    <button-completati />
  </div>
</template>

<script>

export default {
  name: "Home",
  components:{
    'field-add-task': require('@/components/Todo/FieldAddTask.vue').default,
    'list-tasks': require('@/components/Todo/ListTasks.vue').default,
    'no-task': require('@/components/Todo/NoTasks.vue').default,
    'button-completati': require('@/components/Todo/CompletatiButton.vue').default
  }
};
</script>
