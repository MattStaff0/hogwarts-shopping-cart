<template>
  <!-- this is the mustace notation which is placeholder that will get its value from the script -->
  <div>{{ message }}</div>
  <hr />
  <h1>{{ number }}</h1>
  <hr />
  <h2>doubleNumber(50): {{ doubleNumber(number) }}</h2>
  <hr />
  <h2>
    {{
      number > 150
        ? "Number is greater than 150"
        : "Number is less than or equal to 150"
    }}
  </h2>
  <hr />
  <h1>{{ harry }}</h1>
  <h1>{{ harry.name }}</h1>
  <h1>{{ harry.house }}</h1>
  <hr />
  <h2>{{ hogwartsWizards }}</h2>
  <h2>{{ hogwartsWizards[1] }}</h2>
  <hr />
  <br />
  <!-- similar to mustace notation will render the stuff as text -->
  <h1 v-text="number"></h1>
  <hr />
  <br />
  <h1 v-text="rawHtml"></h1>
  <h1 v-html="rawHtml"></h1>
</template>

<script setup>
// values in the script
let message = "Hello world";
let number = 149;

// function that doubles the number
function doubleNumber(number) {
  return number * 2;
}

// defining object
let harry = {
  id: 1001,
  name: "Harry Potter",
  house: "Gryffindor",
  age: 17, // Age during the final battle of Hogwarts
  wand: {
    core: "Phoenix feather",
    wood: "Holly",
  },
};
const hogwartsWizards = [
  {
    id: 1001,
    name: "Harry Potter",
    house: "Gryffindor",
    age: 17,
    wand: {
      core: "Phoenix feather",
      wood: "Holly",
    },
  },
  {
    id: 1002,
    name: "Hermione Granger",
    house: "Gryffindor",
    age: 17,
    wand: {
      core: "Dragon heartstring",
      wood: "Vine",
    },
  },
  {
    id: 1003,
    name: "Ron Weasley",
    house: "Gryffindor",
    age: 17,
    wand: {
      core: "Unicorn hair",
      wood: "Willow",
    },
  },
  {
    id: 1004,
    name: "Draco Malfoy",
    house: "Slytherin",
    age: 17,
    wand: {
      core: "Dragon heartstring",
      wood: "Hawthorn",
    },
  },
];

let rawHtml = '<span style="color: red">This should be red.</span>';
</script>

<style lang="scss" scoped></style>
