<script setup>
import { NCard, NGrid, NFormItemGi, NSelect, NSwitch } from 'naive-ui'
import { language, enterToSend, gptVersion, gptVersions } from '../settings'

const languages = [
  { label: 'English', value: 'en-US' },
  { label: '简体中文', value: 'zh-CN' }
]
</script>

<template>
  <div class="page">
    <n-card :title="$t('ui.ui')">
      <n-grid cols="1 400:2 600:3 800:4 1000:5 1200:6" x-gap="20">
        <n-form-item-gi :label="$t('ui.language')">
          <n-select :options="languages" v-model:value="language" />
        </n-form-item-gi>
        <n-form-item-gi :label="$t('ui.gptVersion')">
          <n-select :options="gptVersions" v-model:value="gptVersion" />
        </n-form-item-gi>
        <n-form-item-gi :label="$t('ui.enterToSend')">
          <n-switch v-model:value="enterToSend" />
        </n-form-item-gi>
      </n-grid>
    </n-card>
  </div>
</template>