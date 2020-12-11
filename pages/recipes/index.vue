<template lang="">
  <div class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :previewText="recipe.id"
    />
  </div>
</template>
<script>
import Recipe from "@/components/Recipe";
export default {
  components: {
    Recipe
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Fruits, Veggies, and Grains",
              previewText: "Protein, Carbs, and Fat",
              thumbnail:
                "https://home.bt.com/images/going-vegan-here-are-5-of-the-best-sources-of-omega-3-you-need-to-know-about-136428079331802601-180628190022.jpg"
            },
            {
              thumbnail: "https://wallpaperaccess.com/full/2004512.jpg",
              title: "Salad",
              id: "2",
              previewText: "Make your own!"
            },
            {
              thumbnail: "https://vegoutmag.com/images/food_and_drink/238.jpg",
              title: "Burrito",
              id: "3",
              previewText: "Add whatever mixture you would like!"
            },
            {
              thumbnail:
                "https://assets.bonappetit.com/photos/5e4c58a55f0567000a32b827/1:1/w_3635,h_3635,c_limit/HLY_Vegan%20Alfredo_Lede.jpg",
              title: "Pasta",
              id: "4",
              previewText: "Add any spices you need"
            },
            {
              thumbnail:
                "https://www.wallpapertip.com/wmimgs/234-2340086_vegan-food-healthy-health-and-smoothie-hd-4k.jpg",
              title: "Acai Bowl",
              id: "5",
              previewText: "Tastes like chocolate some how"
            }
          ]
        });
      }, 1000);
    });
  }
};
</script>
<style>
.recipes {
  display: flex;
  flex-flow: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}
.recipe {
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px grey;
  margin: 30px;

  height: 300px;
}
.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>
