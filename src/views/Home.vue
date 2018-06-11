<template>
  <div class="home">
    <b-container>
      <b-card
        class="text-center">
        <h1>Hello World</h1>
        <b-container fluid id="cards-container">
          <b-row>
            <template v-for="i in 3">
                <b-col :key="i" class="text-left">
                  <b-card header="Test">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Similique dolor, soluta, expedita unde commodi aperiam adipisci dolore animi quaerat repellat rem ea error numquam? Omnis eaque inventore delectus dolorum quam.
                  </b-card>
                </b-col>
            </template>
          </b-row>
        </b-container>
      </b-card>
    </b-container>
  </div>
</template>

<style lang="scss" scoped>
  .container {
    margin-top: 1rem;
  }
  #cards-container {
    margin-top: 2rem;

    .card {
      backface-visibility: hidden;
      &:hover {
        box-shadow: 5px 5px 5px rgba($color: #000000, $alpha: 0.6);
        transform: scale(1.005);
        transition: all .25s linear;

      }
    }

  }
</style>
