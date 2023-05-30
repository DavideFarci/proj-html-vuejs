<script>
export default {
  props: {
    dataNav: Array,
  },
};
</script>

<template>
  <nav>
    <ul>
      <li v-for="item in dataNav">
        <a :href="item.link">{{ item.title }}</a>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
nav {
  ul {
    display: flex;
    align-items: center;
    gap: 2rem;
    list-style: none;
    padding: 0.5rem;
    font-size: 1.1em;
    a {
      text-decoration: none;
      color: white;
      &:hover {
        color: #f9aa01;
      }
    }
  }
}
</style>
