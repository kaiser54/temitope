<template>
  <nav>
    <ul>
      <li class="one">
        <nuxt-link to="/">
          <span class="material-symbols-sharp"> home </span>
          Home
        </nuxt-link>
      </li>
      <li class="two">
        <nuxt-link to="/about"
          ><span class="material-symbols-sharp"> person </span>About
          me</nuxt-link
        >
      </li>
      <li class="three">
        <nuxt-link to="/projects"
          ><span class="material-symbols-sharp"> code </span
          >Projects</nuxt-link
        >
      </li>
      <li class="four">
        <nuxt-link to="/others"
          ><span class="material-symbols-sharp"> electric_bolt </span>Other
          stuffs</nuxt-link
        >
      </li>
      <span class="hover__class"></span>
    </ul>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
nav {
  font-size: 0.7rem;
  line-height: 1.25rem;
  font-weight: 500;
  text-transform: uppercase;
}

a {
  text-decoration: none;
  color: #d9d9d9;
  color: rgba(142, 142, 160);
}

ul {
  list-style: none;
  display: flex;
  flex-direction: row;
  align-items: center;
  background-color: rgb(33, 35, 37);
  background-color: rgba(32, 33, 35);
  border-radius: 16px;
  border-radius: 0.75rem;
  padding: 6px;
  padding: 0.25rem;
  height: 50px;
  align-content: center;
  justify-content: space-between;
  max-width: 488px;
  width: 100%;
  gap: 6px;
  gap: 0.25rem;
}

ul li {
  display: flex;
  flex: 1 0 0px;
  width: 25%;
  height: 40px;
  border-radius: 10px;
  transition: 0.2s ease-in-out;
  color: rgba(142, 142, 160);
  position: relative;
  z-index: 2;
}

ul li a {
  height: 100%;
  width: 100%;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2px;
}

.hover__class {
  height: 40px;
  width: 23%;
  margin-left: 0;
  opacity: 0;
  border-radius: 12px;
  background-color: rgba(79, 82, 84, 0.288);
  position: absolute;
  z-index: 1;
  transition: .5s ease-in-out;
}
.one:hover ~ .hover__class {
  margin-left: 0%;
  opacity: 1;
}
.two:hover ~ .hover__class {
  margin-left: 25%;
  opacity: 1;
}
.three:hover ~ .hover__class {
  margin-left: 50%;
  opacity: 1;
}
.four:hover ~ .hover__class {
  margin-left: 75%;
  opacity: 1;
}

/* li:hover {
  background-color: rgba(79, 82, 84, 0.288);
} */
li:hover a {
  color: rgba(236, 236, 241);
}

.router-link-active.router-link-exact-active {
  background-color: rgba(64, 65, 79);
  border: 1px solid rgba(78, 79, 96);
  color: rgba(236, 236, 241);
}

.router-link-active.router-link-exact-active .material-symbols-sharp {
  color: #00dc82;
}

.material-symbols-sharp {
  font-size: 18px;
}
</style>