<template>
  <main v-if="user">
    <h1>Cześć {{ user.name }} :)</h1>
    <h2>Wylosowana osoba to:</h2>
    <h1>{{ user.user }}!</h1>
  </main>
</template>
<script>
export default {
  name: "MainPage",
  data () {
    return {
      token: this.$route.params.id,
      user: null,
      users: [
        { id: 'd08c2624', name: 'Marta', user: 'Andzia' },
        { id: 'b6123341', name: 'Paweł', user: 'Michał W' },
        { id: '3575eae7', name: 'Asia', user: '' },
        { id: '12a29137', name: 'Paweł', user: '' },
        { id: 'c1a3a19e', name: 'Aga', user: '' },
        { id: '49d9a8f7', name: 'Miki', user: '' },
        { id: 'b3ea800d', name: 'Andzia', user: '' },
        { id: 'e93442a0', name: 'Michał', user: '' },
        { id: '171e1736', name: 'Mariola', user: '' },
        { id: 'a44d89f5', name: 'Roman', user: '' },
        { id: '3d72cc0f', name: 'Hubert', user: '' },
        { id: '8f661457', name: 'Ania', user: '' },
        { id: '01143c9a', name: 'Patrycja', user: '' },
        { id: '9af70af2', name: 'Dawid', user: '' },
        { id: 'f70af29a', name: 'Maruda', user: 'Grażynka' }
      ]
    }
  },
  created () {
    this.user = this.users.find(({ id }) => id == this.$route.params.id)
  },
  methods: {},
}
</script>
<style scoped>
main {
  font-family: 'Merienda', cursive;
  text-align: center;
}

h1 {
  font-size: 3rem;
}

h2 {
  font-size: 2rem;
}
</style>

