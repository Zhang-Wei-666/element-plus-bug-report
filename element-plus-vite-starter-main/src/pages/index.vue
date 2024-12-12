<template>
  <div py-10>
    <el-button @click="visible = true">Show Dialog</el-button>

    <el-dialog
      v-model="visible"
    >
      <MelSelect
        v-model="value"
        :options="options"
        style="width: 240px"
      />
      <div v-if="value">value: {{ value }}</div>
    </el-dialog>
  </div>
</template>

<script lang="ts" setup>
  import { MelSelect } from '@mixte/mel-components/mel-select';
  import { ref } from 'vue';
  import 'element-plus/es/components/select/style/index';

  const visible = ref(false);

  const value = ref<string>();

  const options = [
    { label: '选项1', value: '1' },
    { label: '选项2', value: '2' },
    { label: '选项3', value: '3' },
  ];
</script>
