<template>
  <div class="wrapper">
    <data-table api="logs" :columns="columns" :searchables="searchables"></data-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchables: {
        action: 'Action',
        action_type: 'Type',
      },
      columns: [
        {
          prop: 'id',
          label: 'ID',
          width: '80',
        },
        {
          prop: 'user.data.name',
          label: 'User',
        },
        {
          prop: 'action',
          label: 'Action',
        },
        {
          prop: 'action_type',
          label: 'Type',
        },
        {
          prop: 'created_at',
          label: 'Created At',
        },
      ],
    }
  }
}
</script>

<style lang="scss" scoped>
  .wrapper {
    padding: 20px;
  }
</style>
