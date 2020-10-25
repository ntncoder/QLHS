<template>
  <div class="toolbar">
    <md-toolbar>
      <div class="toolbar-left">
        <md-field>
          <md-select
            v-model="movies"
            name="movies"
            id="movies"
            md-dense
            multiple
          >
            <md-option value="fight-club">Tất cả</md-option>
            <md-option value="godfather">Theo lớp</md-option>
          </md-select>
        </md-field>
      </div>
      <div class="toolbar-right"></div>
    </md-toolbar>
  </div>
</template>

<script>
export default {
  name: "tootbar",
  data() {}
};
</script>

<style lang="scss" scoped>
.toolbar {
  height: 40px;
  width: 100%;
}
.toolbar-left {
  width: 30%;
  height: 100%;
}
.toolbar-right {
  width: 70%;
  height: 100%;
}
</style>