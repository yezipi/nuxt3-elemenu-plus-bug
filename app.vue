<script setup lang="ts">
  import { ElDropdown, ElDropdownItem, ElDropdownMenu, ElIcon, ElSelect, ElOption } from 'element-plus'
  import { ArrowDown } from '@element-plus/icons-vue'
  
  const value = ref('')

  const options = [
    {
      value: 'Select Option1',
      label: 'Select Option1',
    },
    {
      value: 'Select Option2',
      label: 'Select Option2',
    },
    {
      value: 'Select Option3',
      label: 'Select Option3',
    },
    {
      value: 'Select Option4',
      label: 'Select Option4',
    },
    {
      value: 'Select Option5',
      label: 'Select Option5',
    },
  ]
</script>

<template>
  <div class="element-plus-demo" style="padding: 100px">
      <div>
        <h1>Dropdown 组件：</h1>
        <el-dropdown>
        <div class="el-dropdown-link">
          first Dropdown
          <el-icon class="el-icon--right">
            <arrow-down />
          </el-icon>
        </div>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item style="color: green">Dropdown first 1</el-dropdown-item>
            <el-dropdown-item style="color: green">Dropdown first 2</el-dropdown-item>
            <el-dropdown-item style="color: green">Dropdown first 3</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>


      <el-dropdown>
        <div class="el-dropdown-link" style="margin-left: 100px">
          second Dropdown
          <el-icon class="el-icon--right">
            <arrow-down />
          </el-icon>
        </div>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item style="color: red">Dropdown second 1</el-dropdown-item>
            <el-dropdown-item style="color: red">Dropdown second 2</el-dropdown-item>
            <el-dropdown-item style="color: red">Dropdown second 3</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>


    <div>
      <h1>Select 组件：</h1>
      <el-select v-model="value" class="m-2" placeholder="Select" size="large">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        />
      </el-select>
      <el-select v-model="value" class="m-2" placeholder="Select">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        />
      </el-select>
      <el-select v-model="value" class="m-2" placeholder="Select" size="small">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        />
      </el-select>
    </div>

    <p style="margin-top:100px;color: #999">可以看到，下拉部分全部重叠了</p>

  </div>
</template>

<style scoped>
.example-showcase .el-dropdown-link {
  cursor: pointer;
  color: var(--el-color-primary);
  display: flex;
  align-items: center;
}
</style>
