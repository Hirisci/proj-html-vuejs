<template>
  <ul>
    <li v-for="(link, i) in links" :key="i" :class="{ active: link.isActive }">
      <a href="#">{{ link.txt }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "MNav",
  data() {
    return {
      links: [
        {
          txt: "Home",
          isActive: true,
        },
        {
          txt: "Serie Tv",
          isActive: false,
        },
        {
          txt: "Film",
          isActive: false,
        },
        {
          txt: "Nuovi e popolari",
          isActive: false,
        },
        {
          txt: "La mia lista",
          isActive: false,
        },
        {
          txt: "Audio e sottotitoli",
          isActive: false,
        },
      ],
    };
  },
};
</script>


<style lang="scss" scoped>
ul {
  display: flex;
  gap: 1rem;
  color: var(--clr-txt-2);

  a {
    color: inherit;
    text-decoration: none;
    &:hover {
      color: var(--clr-txt-3);
    }
  }
}
.active {
  color: var(--clr-txt-1);
}
</style>