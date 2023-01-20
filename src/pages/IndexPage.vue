<template>
  <q-page class="flex flex-center" style="padding: 5%;">
    <q-card style="width:800px; height:auto">
      <q-card-section>
        <div class="text-h2" style="font-family: 'Tourney', cursive; color:green; text-align: end;">
          O naturalismo</div>
        <q-separator class="q-mb-md" />
        <div class="text-subtitle" style="font-size: 20px; text-align:end; color: grey; margin-bottom: 150px;">bem
          perto de você, vem
          se
          divertir !
        </div>

        <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md">

          <q-input filled v-model="name" label="Your name *" hint="Name and surname" lazy-rules
            :rules="[val => val && val.length > 0 || 'Please type something']" />

          <q-input filled v-model="name" label="Your name *" hint="Name and surname" lazy-rules
            :rules="[val => val && val.length > 0 || 'Please type something']" />

          <q-input filled v-model="name" label="Your name *" hint="Name and surname" lazy-rules
            :rules="[val => val && val.length > 0 || 'Please type something']" />

          <q-input filled v-model="name" label="Your name *" hint="Name and surname" lazy-rules
            :rules="[val => val && val.length > 0 || 'Please type something']" />

          <q-toggle v-model="accept" label="I accept the license and terms" />

          <div>
            <q-btn label="Gravar" type="submit" color="primary" />
            <q-btn label="Limpar" type="reset" color="warning" flat class="q-ml-sm" />
          </div>
        </q-form>
      </q-card-section>

    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
