<template>
  <Layout name="LayoutDefault">

    <About  />

  </Layout>
</template>
<script>
import Layout from "@/layouts/Layout";
import About from "@/components/About.vue"
export default {
  components: { Layout,About },
};
</script>
