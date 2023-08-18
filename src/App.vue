<script>
import { RouterLink, RouterView } from 'vue-router'
import WelcomeMessage from './components/WelcomeMessage.vue'
export default {
  components: {
    WelcomeMessage
  }
}
</script>

<template>
  <header>
    <h1>Todo</h1>
    <div class="wrapper">
      <WelcomeMessage
        msg="I made a huge to do list for today, I just can't figure out who is going to do it"
      />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <Suspense>
    <RouterView />

    <template #fallback> Loading... </template>
  </Suspense>
</template>

<style scoped>
header h1 {
  color: #db6b97;
  font-weight: 800;
  font-size: 3rem;
}
header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  line-height: 1.5;
  max-height: 100vh;
  margin-bottom: 2rem;
}

header .wrapper {
  display: flex;
  place-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-bottom: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    padding-right: calc(var(--section-gap) / 2);
    margin-top: 0;
  }

  nav {
    /* text-align: left; */
    /* margin-left: -1rem; */
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
