<template>
  <q-modal ref="addNoteModal">
    <h6 class="on-right">Új jegyzet</h6>

    <div class="fields">
      <q-field>
        <q-input v-model="note" type="textarea" />
      </q-field>
    </div>

    <div class="row justify-around buttons">
      <q-btn color="primary" @click="$refs.addNoteModal.close()">Mégse</q-btn>
      <q-btn color="indigo-7" @click="addNote">Hozzáadás</q-btn>
    </div>
  </q-modal>
</template>

  <script>
    import {
      QModal,
      QField,
      QInput,
      QBtn,
    } from 'quasar';

    export default {
      data() {
        return {
          note: '',
        };
      },
      methods: {
        open() {
          this.note = '';
          this.$refs.addNoteModal.open();
        },
        addNote() {
          console.log(this.note);
        },
      },
      components: {
        QModal,
        QField,
        QInput,
        QBtn,
      },
    };

  </script>

  <style scoped>
    .fields {
      width: 90%;
      margin: auto;
    }

    .buttons {
      margin-top: 30px;
    }

  </style>
