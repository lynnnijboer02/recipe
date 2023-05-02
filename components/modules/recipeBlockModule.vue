
<template>
    <div class="recipeBlockModule">
      <div class="container">
        <h3 class="recipeBlockModule__title">Recipes</h3>
        <div class="recipeBlockModule__recipeBlocks">
          <recipeBlock 
            v-for="(recipeBlock, index) in recipeBlocks" 
            :key="index" 
            :text="recipeBlock.text" 
            :title="recipeBlock.title"
            :time="recipeBlock.time"
            :img="recipeBlock.img"
            :kcal="recipeBlock.kcal"
            :slug="recipeBlock.slug"
          />
        </div>
      </div>
    </div>
</template>

<script>

export default {
  name: 'recipeBlockModule',
  props: {
    recipeBlocks: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.recipeBlockModule {
  padding: {
    top: rem(100px);
    bottom: rem(100px);
  }

  &__title {
    display: flex;
    justify-content: center;
    margin-bottom: 40px;
  }

  &__recipeBlocks {
    display: grid;
    grid-template-columns: 1fr;
    gap: 40px;

    @include media-breakpoint-up(lg) {
      grid-template-columns: 1fr 1fr;
    }
  }
}
</style>
