<script setup>
import { ref, computed } from 'vue'


const course = "Web Systems"
const instructor = "Mr. Reyes"
const room = "Lab 2"

const quizScore = 18
const perfectScore = 20

const percentage = computed(() => {
  return (quizScore / perfectScore) * 100
})

const score = ref(0)

function addPoint() {
  score.value++
}

const isOpen = ref(false)

function changeStatus() {
  isOpen.value = !isOpen.value
}

const schoolLogo =
  "https://www.materdeicollege.com/"

const portal = "https://www.google.com"

const isEnrollDisabled = true
</script>

<template>
  <div style="font-family: Arial; padding:20px;">

    <!-- Task 1 -->
    <h2>Task 1</h2>
    <h3>Course Information</h3>

    <p><b>Course:</b> {{ course }}</p>
    <p><b>Instructor:</b> {{ instructor }}</p>
    <p><b>Room:</b> {{ room }}</p>

    <hr>

    <!-- Task 2 -->
    <h2>Task 2</h2>

    <p><b>Quiz Score:</b> {{ quizScore }}</p>
    <p><b>Perfect Score:</b> {{ perfectScore }}</p>

    <p><b>Percentage:</b> {{ percentage }}%</p>

    <hr>

    <!-- Task 3 -->
    <h2>Task 3</h2>

    <p><b>Score:</b> {{ score }}</p>

    <button @click="addPoint">
      Add Point
    </button>

    <hr>

    <!-- Task 4 -->
    <h2>Task 4</h2>

    <p><b>Class Status:</b> {{ isOpen ? "Open" : "Closed" }}</p>

    <button @click="changeStatus">
      Change Status
    </button>

    <hr>

    <!-- Task 5 -->
    <h2>Task 5</h2>

    <img
      :src="schoolLogo"
      alt="School Logo"
      width="150"
    >

    <hr>

    <!-- Task 6 -->
    <h2>Task 6</h2>

    <a :href="portal" target="_blank">
      Visit School Portal
    </a>

    <hr>

    <!-- Task 7 -->
    <h2>Task 7</h2>

    <button :disabled="isEnrollDisabled">
      Enroll
    </button>

  </div>
</template>