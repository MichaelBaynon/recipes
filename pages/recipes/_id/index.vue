<template lang="">
  <div>
    <nuxt-link class="go-back-link" to="/recipes">Go back to recipes</nuxt-link>
    <section class="single-recipe">
      <div class="text-area">
        <h1 class="recipe-title">{{ recipe.title }}</h1>
        <p>{{ recipe.descriptionText }}</p>
      </div>
      <div>
        <img class="recipe-img" :src="recipe.thumbnail" :alt="recipe.title" />
      </div>
    </section>
  </div>
</template>
<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Fruits, Veggies, and Grains",
              previewText: "Protein, Carbs, and Fat",
              descriptionText: "a great meal",
              thumbnail:
                "https://home.bt.com/images/going-vegan-here-are-5-of-the-best-sources-of-omega-3-you-need-to-know-about-136428079331802601-180628190022.jpg"
            },
            {
              thumbnail: "https://wallpaperaccess.com/full/2004512.jpg",
              title: "Salad",
              id: "2",
              descriptionText: "Make your own!",
              previewText: "Make your own!"
            },
            {
              thumbnail: "https://vegoutmag.com/images/food_and_drink/238.jpg",
              title: "Burrito",
              id: "3",
              descriptionText: "Add whatever mixture you would like!",
              previewText: "Add whatever mixture you would like!"
            },
            {
              thumbnail:
                "https://assets.bonappetit.com/photos/5e4c58a55f0567000a32b827/1:1/w_3635,h_3635,c_limit/HLY_Vegan%20Alfredo_Lede.jpg",
              title: "Pasta",
              id: "4",
              descriptionText: "Add any spices you need",
              previewText: "Add any spices you need"
            },
            {
              thumbnail:
                "https://www.wallpapertip.com/wmimgs/234-2340086_vegan-food-healthy-health-and-smoothie-hd-4k.jpg",
              title: "Acai Bowl",
              id: "5",
              descriptionText: "Tastes like chocolate some how",
              previewText: "Tastes like chocolate some how"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1500);
    });
  }
};
</script>
<style>
.single-recipe {
  display: flex;
  flex-flow: row;
  justify-content: space-around;

  padding: 30px;

  width: 70%;
  margin: 0 auto;
  margin-top: 100px;
}

.text-area {
  padding-left: 200px;
  padding-top: 50px;
}

.recipe-img {
  width: 50%;
  box-shadow: 5px 5px 15px grey;
  margin-left: 40%;
  border-radius: 5px;
}

.recipe-title {
  border-left: 2px solid #03abff;
  background: #bde9ff;
  margin-bottom: 30px;
  padding: 2px 8px;
  font-size: 50px;
}
.go-back-link {
  margin-left: 200px;
  color: green;
}
.go-back-link:hover {
  color: #30c96e;
}
</style>
