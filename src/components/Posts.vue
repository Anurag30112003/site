<script>
import { RouterLink, RouterView } from "vue-router";
import MakePost from "@/components/MakePost.vue";
export default {
  name: "Posts",
  components: {
    MakePost,
    RouterLink,
    RouterView,
  },
};
</script>
<template>
  <div class="posts">
    <div class="title">Posts</div>
    <!-- post start -->
    <div class="box">
    <MakePost
      title="Web3 vs Inflation"
      body="How Decentralisation and Web3 can beat inflation ?"
    />
    <div class="rt">  <router-link to="/1" class="btn">Read-More</router-link> </div>
    </div>
    <!-- post end -->
       <!-- post start -->
    <div class="box">
    <MakePost
      title="Are we in a simulation ?"
      body="Is the world we are living in is a computer simulation ?"
    />
    <div class="rt">  <router-link to="/2" class="btn">Read-More</router-link> </div>
    </div>
    <!-- post end -->
  </div>
</template>
<style scoped>
.rt{
  text-align: center;
  padding-bottom  : 3rem;
}
.btn{
  background-color: var(--third);
  color: var(--primary);
  padding: 1rem 1.5rem;
  text-decoration: none;
  font-family: "Josefin Sans", sans-serif;
  font-size: 1.3rem;
}
.btn:hover{
  color: var(--third);
  background-color: var(--primary);
  border: 2px solid var(--third);
}
.box{
    outline-style: solid;
  outline-color: var(--third);
  outline-width: 2px;
}
.title {
  font-size: 40px;
  font-weight: 400;
  font-family: "Josefin Sans", sans-serif;
  padding-bottom: 10px;
  text-align: center;
  text-decoration: underline;
  text-decoration-color: var(--third);
}
@media only screen and (max-width: 420px) {
  .title {
    font-size: 30px;
  }
  .btn{
    font-size: 1rem;
      padding: 0.5rem 1rem;

  }
  .rt{
      padding-bottom  : 1.4rem;

  }

}
</style>
