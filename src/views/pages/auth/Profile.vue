<template>
  <Layout name="LayoutDefault">
    <div>
      <div class="d-flex bd-highlight" v-if="isLogin">
        <div class="p-2 flex-grow-1 bd-highlight">
          <update-profile></update-profile>
        </div>
        <div class="p-2 bd-highlight flex-lg-grow-1">
          <update-password></update-password>
        </div>
      </div>
    </div>
  </Layout>
</template>
<script>
  import Layout from "@/layouts/Layout";
  import UpdatePassword from "@/components/auth/UpdatePassword";
  import UpdateProfile from "@/components/auth/UpdateProfile";

  export default {
    components: { Layout, UpdatePassword, UpdateProfile },
    computed: {
      isLogin() {
        return this.$store.getters["login/isLogin"];
      },
      user() {
        return this.$store.getters.user;
      },
    },
  };
</script>
