<script>
let skills=[
  {
    id:1,
    name:'html'
  },
  {
    id:2,
    name:'vuejs'
  },
  {
    id:3,
    name:'nodeJs'
  },
  {
    id:4,
    name:'Express'
  },
  {
    id:5,
    name:'Jwt'
  },
  {
    id:6,
    name:'Morgan'
  }
];
</script>

<style>
.Skill {
  display: flex;
  align-items:center;
  justify-content: center;
}
ul{
  margin: 0;
  padding: 0;
  list-style:none;
}
li{
  display: inline;
  margin: 0 0 0 0.4em;
}
</style>

<div class="Skills">
<h3>Habilidades</h3>

{#each skills as {name},i}

<li>{name}</li>

{/each}

</div>