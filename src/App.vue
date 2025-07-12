<template>
  <main class="main">
    <h1>Note App</h1>

    <div class="notes">
      <Card 
        v-for="item in notes" 
        :title="item.title" 
        :content="item.content" 
        :time="item.time" 
      />
    </div>

    <AddButton @click="togglePopup" />

    <AddNewNote 
      v-if="isVisible"
      @onClose="togglePopup" 
      @onSave="addNote" 
     />
  </main>
</template>

<script setup>
import Card from './components/Card.vue'
import AddButton from './components/AddButton.vue';
import AddNewNote from './components/AddNewNote.vue';
import { ref } from 'vue';

const isVisible = ref(false);
const notes = ref([])

function addNote(title, content) {
  let note = {
    title: title,
    content: content,
    time: (new Date()).toLocaleDateString()
  }

  notes.value.push(note);
}

const togglePopup = () => {
  isVisible.value = !isVisible.value
}

</script>

<style>
body,
#app {
  width: 100%;
  height: 100%;
  color: #000;
}

main.main {
  background: linear-gradient(128deg, rgba(135, 246, 180, 0.84) 12.75%, rgba(50, 180, 187, 0.67) 83.4%);
  width: 100%;
  min-height: 100vh;
  padding: 24px;
}

h1 {
  font-family: Inter;
  font-weight: 700;
  font-style: Bold;
  font-size: 32px;
  line-height: 100%;
  letter-spacing: 0%;
  text-align: center;
  padding: 24px;
}

.notes {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  gap: 26px;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
