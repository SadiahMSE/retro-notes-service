<template>
<div id="noteEntry">
    <span>Note: </span>
    <ul id="noteList">
        <li v-for="note in notes">
            {{note.date | dateFormat('YYYY.MM.DD')}}
            {{note.message}}
        </li>
    </ul>
    <br>
    <textarea v-model="message" placeholder="Add in retro notes for today"></textarea>
    <button v-on:click="addNote">Submit</button>
</div>
</template>

<script>
import Vue from 'vue'
import VueFilterDateFormat from 'vue-filter-date-format'

Vue.use(VueFilterDateFormat)

 export default {
     data: function() {
         return { 
             message : "",
             notes: [
                 {date: new Date("28-08-2018"), message: "Hi"},
                 {date: new Date("29-08-2018"), message: "Hi there"}
             ]
         }
     },
     methods: {
        addNote: function (event) {
            this.notes.push({date: new Date(), message: this.message});
        }
     }
 }
</script>

<style>
    #noteEntry {
        color: black;
        margin: 1rem;
        padding: 1rem;
    }
</style>