<template>
<div id="noteEntry">
    <span>Note: </span>
    <ul id="noteList">
        <li v-for="note in notes">
            {{note.date | dateFormat}}
            {{note.message}}
        </li>
    </ul>
    <br>
    <textarea v-model="message" placeholder="Add in retro notes for today"></textarea>
    <button v-on:click="addNote">Submit</button>
</div>
</template>

<script>
 export default {
     data: function() {
         return { 
             message : "",
             notes: [
                 {date: new Date("2018-08-20"), message: "Hi"},
                 {date: new Date("29-08-2018"), message: "Hi there"}
             ]
         }
     },
     methods: {
        addNote: function(event) {
            this.notes.push({date: new Date(), message: this.message});
        }
     },
     filters: {
         dateFormat: function (date) {
             return date.getFullYear() + '-' + (date.getMonth() + 1) + '-' + date.getDate();
         }
     }
 }
</script>

<style>
    #noteEntry {
        color: black;
        margin: 1rem;
        padding: 1rem;
        top: 0px;
    }
</style>