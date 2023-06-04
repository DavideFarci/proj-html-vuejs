<script>
export default {
  props: {
    dataNav: Object,
  },
};
</script>

<template>
  <nav>
    <ul class="d-flex">
      <li v-for="item in dataNav" :key="item.id">
        <div class="dropdown">
          <a
            class="btn"
            :href="item.link"
            role="button"
            data-bs-toggle="dropdown"
            aria-expanded="false"
          >
            {{ item.title }}
          </a>

          <ul class="dropdown-menu bg-dark">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </div>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
nav {
  ul {
    // display: flex;
    // align-items: center;
    // gap: 2rem;
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
