<template>
  <div>
    <h1>dashboard</h1>
    <DynamicContent>
      <em>Slot do component DynamicContent</em>
      <hello-world msg="Teste Hotjar + Fragment in Vue2" />
    </DynamicContent>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue';
import DynamicContent from '../components/DynamicContent.vue';
export default {
  name: 'Dashboard',
  components: { DynamicContent, HelloWorld }
}
</script>