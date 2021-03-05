<template>
  <v-app>
    <v-app-bar app color="green">
      <v-btn text to="/">Home</v-btn>
      <v-btn text to="/decks">Decks</v-btn>
      <v-btn text to="/profile">Profile</v-btn>
      <v-btn text to="/settings">Settings</v-btn>
    </v-app-bar>
  </v-app>
<!--  <header>-->
<!--    <nav>-->
<!--      <ul>-->
<!--        <li>-->
<!--          <nuxt-link to="/">-->
<!--            Home-->
<!--          </nuxt-link>-->
<!--        </li>-->
<!--        <li>-->
<!--          <nuxt-link to="/decks">-->
<!--            Decks-->
<!--          </nuxt-link>-->
<!--        </li>-->
<!--        <li>-->
<!--          <nuxt-link to="/profile">-->
<!--            Profile-->
<!--          </nuxt-link>-->
<!--        </li>-->
<!--        <li>-->
<!--          <nuxt-link to="/settings">-->
<!--            Settings-->
<!--          </nuxt-link>-->
<!--        </li>-->
<!--      </ul>-->
<!--    </nav>-->
<!--  </header>-->
</template>

<style scoped>
  header {
    background: black;
    color: white;
    height: 60px;
  }

  header ul {
    align-items: center;
    display: flex;
    justify-content: center;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  header ul li {
    margin: auto 1.5rem;
  }
</style>
