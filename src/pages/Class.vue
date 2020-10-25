<template>
  <div class="content">
    <div
      class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100"
    >
      <md-card class="md-card-plain">
        <md-card-header data-background-color="green">
          <h4 class="title">Danh sách lớp học</h4>
        </md-card-header>
        <md-card-content>
          <class-list></class-list>
        </md-card-content>
      </md-card>
    </div>
  </div>
</template>

<script>
//import { SimpleTable, OrderedTable } from "@/components";
import ClassList from "./class/class-list";

export default {
  components: {
    //OrderedTable,
    ClassList
  },
  data() {
    return {
      className: ""
    };
  }
};
</script>
