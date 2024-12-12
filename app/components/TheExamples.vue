<script setup lang="ts">
  import { ElMessageBox } from 'element-plus';
  import { ref } from 'vue';

  const { appContext } = getCurrentInstance()!;

  const visible = ref(false);

  function onClick() {
    ElMessageBox.prompt('Hello World');
    // ElMessageBox.prompt('Hello World', appContext);
  }
</script>

<template>
  <div py-10>
    <el-button @click="visible = true">Show Dialog</el-button>

    <el-dialog
      v-model="visible"
    >
      <el-button @click="onClick">
        Click me
      </el-button>
    </el-dialog>
  </div>
</template>
