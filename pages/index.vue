<template>
    <div class="modules">
      <modules :modules="modules"/>
    </div>
</template>

<script>

export default {
  name: 'IndexPage',
  data() {
    return {
      data() {
        return {
          currentPage: {},
        };
      },
      async fetch() {
        const { items } = await this.$contentful.getEntries({
          content_type: 'homepage',
          include: 4,
        });

        [this.currentPage] = items;
      },
      modules: [
        {
          type: 'hero',
          title: 'Find here low calorie recipes',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
          buttonColor: 'alpha',
          secondButtonColor: '',
          buttonText: 'All recipes',
          secondButtonText: 'Contact me',
        },
        {
          type: 'recipeBlock',
          recipeBlocks: [
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '30 min',
              kcal: '260kcal',
              img: 'https://images.pexels.com/photos/699953/pexels-photo-699953.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '25 min',
              kcal: '340kcal',
              img: 'https://images.pexels.com/photos/376464/pexels-photo-376464.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '40 min',
              kcal: '630kcal',
              img: 'https://images.pexels.com/photos/2097090/pexels-photo-2097090.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '25 min',
              kcal: '520kcal',
              img: 'https://images.pexels.com/photos/2116094/pexels-photo-2116094.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '30 min',
              kcal: '260kcal',
              img: 'https://images.pexels.com/photos/699953/pexels-photo-699953.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '25 min',
              kcal: '340kcal',
              img: 'https://images.pexels.com/photos/376464/pexels-photo-376464.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '40 min',
              kcal: '630kcal',
              img: 'https://images.pexels.com/photos/2097090/pexels-photo-2097090.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
            {
              title: 'Recept naam',
              text: 'Marketing content creation for brands & individuals. Providing graphic design.',
              time: '25 min',
              kcal: '520kcal',
              img: 'https://images.pexels.com/photos/2116094/pexels-photo-2116094.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2',
              slug: 'hallo'
            },
          ]
        },
        {
          type: 'textBlock',
          textBlocks: [
            {
              title: 'Benodigdheden & bereiding',
              ingredients: [
                {
                  recipe: '1 ei'
                },
                {
                  recipe: '40g eiwit'
                },
                {
                  recipe: '10g bloem'
                },
                {
                  recipe: '10ml olijfolie'
                },
              ],
              listItems: [
                {
                  step: 'Step 1',
                  instructions: 'CO-DA Studios is a digital media content production company specializing in marketing content creation for brands & individuals.',
                  img: 'https://images.pexels.com/photos/2116094/pexels-photo-2116094.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
                },
                {
                  step: 'Step 2',
                  instructions: 'CO-DA Studios is a digital media content production company specializing in marketing content creation for brands & individuals.',
                  img: 'https://images.pexels.com/photos/5894552/pexels-photo-5894552.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
                },
                {
                  step: 'Step 3',
                  instructions: 'CO-DA Studios is a digital media content production company specializing in marketing content creation for brands & individuals.',
                  img: 'https://images.pexels.com/photos/4781414/pexels-photo-4781414.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
                },
              ]
            },
          ]
        },
      ]
    }
  }
}
</script>
