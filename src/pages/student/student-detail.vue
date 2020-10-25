<template>
  <div class="student-form">
    <md-dialog :md-active.sync="showDialog">
      <md-dialog-title>Học sinh</md-dialog-title>
      <md-field>
        <label>Họ và tên</label>
        <md-input v-model="regular" md-counter="30"></md-input>
      </md-field>
      <md-field>
        <label>Ngày sinh</label>
        <md-input v-model="regular" md-counter="30"></md-input>
      </md-field>
      <md-field>
        <label>Lớp</label>
        <md-input v-model="regular" md-counter="30"></md-input>
      </md-field>
      <md-field>
        <label>Giới tính</label>
        <md-input v-model="regular" md-counter="30"></md-input>
      </md-field>
      <md-field>
        <label>Nơi ở</label>
        <md-input v-model="regular" md-counter="30"></md-input>
      </md-field>
      <md-field>
        <label>Số điện thoại phụ huynh</label>
        <md-input v-model="regular" md-counter="30"></md-input>
      </md-field>
    </md-dialog>
  </div>
</template>

<script>
export default {
  name: "student-detail",
  data() {
    showDialog: true
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
</style>