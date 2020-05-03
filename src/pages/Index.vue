<template>
  <q-page class="row justify-evenly">
    <q-parallax
      :height="600"
      src="https://cdna.artstation.com/p/assets/images/images/000/632/544/4k/wavenwater-michael-guimont-storyframe-16-00-ver-07.jpg?1443929476"
    >
      <div class="row q-col-gutter-md q-pa-md">
        <div class="col-12">
          <h3 class="text-primary">Luminarly</h3>
        </div>
        <div class="col-12 col-md-6">
          <p class="text-subtitle1">
            A tool for artists and creatives that allows you to create
            moodboards and collections from images all over the internet under
            Creative Commons license.
          </p>
        </div>
        <div class="col-12 col-md-8">
          <q-input
            dark
            filled
            v-model="text"
            label="Search for projects"
            :readonly="readonly"
            :disable="disable"
          >
            <template v-slot:append>
              <q-icon name="search" class="text-primary cursor-pointer" />
            </template>
          </q-input>
        </div>
      </div>
    </q-parallax>

  </q-page>
</template>

<script lang="ts">
import ExampleComponent from 'components/CompositionComponent.vue';
import { Todo, Meta } from 'components/models';

export default {
  name: 'PageIndex',
  components: {},
  data() {
    const todos: Todo[] = [
      {
        id: 1,
        content: 'ct1'
      },
      {
        id: 2,
        content: 'ct2'
      },
      {
        id: 3,
        content: 'ct3'
      },
      {
        id: 4,
        content: 'ct4'
      },
      {
        id: 5,
        content: 'ct5'
      }
    ];
    const meta: Meta = {
      totalCount: 1200
    };
    return { todos, meta };
  }
};
</script>
