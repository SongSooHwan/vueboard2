<template>
  <div id="header">
    <b-navbar toggleable="lg" type="dark" class="bg-dark" variant="info" >
      <div class="container mb-0">
        <b-navbar-brand to="/">Vue Board</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item to="/">자유게시판</b-nav-item>
            <b-nav-item to="/gallery">갤러리</b-nav-item>
            <b-nav-item to="/boardlist">공지사항/자료실</b-nav-item>
            <b-nav-item to="/calvue">달력</b-nav-item>
          </b-navbar-nav>
          <b-navbar-nav class="ms-auto">
            <b-nav-item-dropdown class="login-list" right>
              <template #button-content>
                <span>User</span>
              </template>
              <b-dropdown-item to="/Login">Login</b-dropdown-item>
              <b-dropdown-item to="/Login">Sign Out</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  </div>
</template>

<script>
export default {
  nama: "Header",
  data() {
    return {

    }
  }
};
</script>
<style>
.login-list .dropdown-menu{right:0;}
</style>
