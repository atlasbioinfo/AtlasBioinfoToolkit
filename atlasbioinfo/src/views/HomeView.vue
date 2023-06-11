<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card v-for=" tcard in toolcards " class="flat bordered">            
      <q-card-section>
        <div class="text-h6">{{ tcard.title }}</div>
      </q-card-section>

      <q-card-section>
        {{ tcard.description }}
      </q-card-section>

      <q-separator dark />

      <q-card-actions>
        <q-btn flat round color="red" icon="add" />
        <q-btn flat round color="blue" icon="favorite" />
        <q-btn flat round color="primary" icon="share" />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'AtlasHomeView',

  setup () {
    const toolcards=[
        {
            title: 'DNA <=> RNA',
            description: 'Sequence conversion, reverse complementarity',
        },
        {
            title: "RNA <=> Protein",
            description: 'Sequence conversion, codon to AAs, vice versa'
        },
        
    ]
    

    return {
        toolcards
    }
  }
}

</script>