
<template>
  <nuxt-link 
    :to="`/recipes/${slug}`"  
    class="recipeBlock w-100"
  >
    <div class="recipeBlock__content text-color-dark">
      <div class="recipeBlock__content--title">
        <h5 class="m-0 h6">{{ title }}</h5>
        <p class="m-0">{{ text }}</p>
      </div>
      <div class="recipeBlock__content--info">
        <p class="mb-0 mt-4">{{ time }}</p>
        <p class="mb-0 mt-4">{{ kcal }}</p>
      </div>
    </div>
    <div 
      class="recipeBlock__image" 
      :style="{ '--bg-img': `url('${img}')` }"
    >
    </div>
  </nuxt-link>
</template>

<script>

export default {
  name: 'recipeBlock',
  props: {
    title: {
      type: String,
      default: "Project",
      required: true
    },
    text: {
      type: String,
      default: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    time: {
      type: String,
      default: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    kcal: {
      type: String,
      default: "350kcal"
    },
    img: {
      type: String,
      default: "https://images.pexels.com/photos/3715605/pexels-photo-3715605.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
    },
    slug: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.recipeBlock {
  box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 6px;
  cursor: pointer;
  border-radius: 2rem;
  background-color: var(--color-light);
  display: grid;
  grid-template-rows: 1fr 1fr;
  grid-template-columns: 1fr;
  overflow: hidden;

  @include media-breakpoint-up(sm) {
    grid-template-columns: 2fr 1.5fr;
    grid-template-rows: 1fr;
    height: 250px;
  }

  &__content {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &--info {
      display: flex;
      opacity: 0.5;
      justify-content: space-between;
    }
  }

  &__image {
    background-image: var(--bg-img);
    background-size: cover;
  }
}
</style>
