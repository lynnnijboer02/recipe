<template>
  <section>
    <div 
      v-for="(module, index) in modules" 
      :key="index">
      <modulesHeroModule 
        v-if="module.type === 'hero'" 
        :title="module.title" :text="module.text" 
        :buttonColor="module.buttonColor" 
        :secondButtonColor="module.secondButtonColor" 
        :buttonText="module.buttonText" 
        :secondButtonText="module.secondButtonText"
      />
      <modulesTextBlockModule 
        v-if="module.type === 'textBlock'" 
        :textBlocks="module.textBlocks" 
      />
      <modulesRecipeBlockModule 
        v-if="module.type === 'recipeBlock'" 
        :recipeBlocks="module.recipeBlocks"
      />
    </div>
  </section>
</template>

<script>

export default {
  name: 'modules',
  props: {
    modules: {
      type: Array,
      required: true
    }
  }
}
</script>
