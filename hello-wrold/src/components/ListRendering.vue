<template>
  <div>
    <h1>array of string</h1>
    <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
    <h1>array of object</h1>
    <h2 v-for="(name, index) in fullNames" :key="index">
      {{ name.firstName }} {{ name.lastName }}
    </h2>
    <h1>array of object nested</h1>
    <div v-for="actor in actors" :key="actor.name">
      {{ actor.name }}
      <h2 v-for="(movie, index) in actor.movies" :key="index">{{ movie }}</h2>
    </div>

    <h1>data property in object</h1>

    <h2 v-for="(value, key, index) in info" :key="index">
      {{ index }} {{ key }} {{ value }}
    </h2>
  </div>

  <template v-for="name in names" :key="name">
    <h1>{{ name }}</h1>
    <br/>
  </template>
</template>

<script>
export default {
  name: "Rendering",
  data() {
    return {
      names: ["asda", "dd", "fff"],
      fullNames: [
        { firstName: "dfsdf", lastName: "dfsdf" },
        { firstName: "sdsd", lastName: "dd" },
        { firstName: "gggg", lastName: "fdfd" },
      ],
      actors: [
        {
          name: "Aizaz",
          movies: ["one", "two"],
        },
        {
          name: "Aziz",
          movies: ["dd", "gg"],
        },
        {
          name: "Tahirani",
          movies: ["yy", "fgf"],
        },
      ],
      info: {
        one: "ss",
        two: "aa",
        three: "asda",
      },
    };
  },
};
</script>
