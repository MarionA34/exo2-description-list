<script setup>
const firstPerson = {
  gender: 'female',
  firstname: 'Emily',
  lastname: 'Parker',
  age: 24,
  job: 'Teacher',
  hobbies: ['read books', 'go hiking'],
  pet: {
    name: 'Whiskers',
    age: 2,
    species: 'ferret',
  },
}

const secondPerson = {
  gender: 'male',
  firstname: 'Marcus',
  lastname: 'Bennett',
  age: 38,
  job: 'Architect',
  hobbies: ['watch bird', 'play chess'],
  pet: {
    name: 'Nala',
    age: 6,
    species: 'dog',
  },
}

const thirdPerson = {
  gender: 'female',
  firstname: 'Sophia',
  lastname: 'Rodriguez',
  age: 31,
  job: 'Environmental scientist',
  hobbies: ['play guitar', 'bake cakes'],
  pet: {
    name: 'Paws',
    age: 3,
    species: 'cat',
  },
}

const fourthPerson = {
  gender: 'male',
  firstname: 'Oliver',
  lastname: 'Hughes',
  age: 56,
  job: 'Carpenter',
  hobbies: ['paint', 'ride horses'],
  pet: {
    name: 'Bubble',
    age: 4,
    species: 'snake',
  },
}
</script>

<template>
  <main class="container">
    <h1>Description list</h1>
    <div class="cards">
      <div class="card">
        <img
          src="./assets/img/emily-parker.jpg"
          alt="{{firstPerson.firstname}} {{firstPerson.lastname}}"
        />
        <h2>{{ firstPerson.firstname }} {{ firstPerson.lastname }}</h2>
        <p>
          {{ firstPerson.gender === 'female' ? 'She' : 'He' }} is a {{ firstPerson.age }}-year-old
          {{ firstPerson.job.toLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ firstPerson.firstname }} likes to {{ firstPerson.hobbies[0] }} and
          {{ firstPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ firstPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{ firstPerson.pet.name }} a {{ firstPerson.pet.age }} years-old
          {{ firstPerson.pet.species }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div class="card">
        <img
          src="./assets/img/marcus-bennett.jpg"
          alt="{{secondPerson.firstname}} {{secondPerson.lastname}}"
        />
        <h2>{{ secondPerson.firstname }} {{ secondPerson.lastname }}</h2>
        <p>
          {{ secondPerson.gender === 'female' ? 'She' : 'He' }} is a {{ secondPerson.age }}-year-old
          {{ secondPerson.job.toLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ secondPerson.firstname }} likes to {{ secondPerson.hobbies[0] }} and
          {{ secondPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ secondPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{ secondPerson.pet.name }} a {{ secondPerson.pet.age }} years-old
          {{ secondPerson.pet.species }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div class="card">
        <img
          src="./assets/img/sophia-rodriguez.jpg"
          alt="{{thirdPerson.firstname}} {{thirdPerson.lastname}}"
        />
        <h2>{{ thirdPerson.firstname }} {{ thirdPerson.lastname }}</h2>
        <p>
          {{ thirdPerson.gender === 'female' ? 'She' : 'He' }} is a {{ thirdPerson.age }}-year-old
          {{ thirdPerson.job.toLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ thirdPerson.firstname }} likes to {{ thirdPerson.hobbies[0] }} and
          {{ thirdPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ thirdPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{ thirdPerson.pet.name }} a {{ thirdPerson.pet.age }} years-old
          {{ thirdPerson.pet.species }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div class="card">
        <img
          src="./assets/img/olivier-hughes.jpg"
          alt="{{fourthPerson.firstname}} {{fourthPerson.lastname}}"
        />
        <h2>{{ fourthPerson.firstname }} {{ fourthPerson.lastname }}</h2>
        <p>
          {{ fourthPerson.gender === 'female' ? 'She' : 'He' }} is a {{ fourthPerson.age }}-year-old
          {{ fourthPerson.job.toLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ fourthPerson.firstname }} likes to {{ fourthPerson.hobbies[0] }} and
          {{ fourthPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ fourthPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{ fourthPerson.pet.name }} a {{ fourthPerson.pet.age }} years-old
          {{ fourthPerson.pet.species }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
    </div>
  </main>
</template>

<style scoped>
.container {
  max-width: 1024px;
  background-color: #cae1c2;
  border-radius: 10px;
  margin: 0 auto;
  font-family:
    'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana,
    sans-serif;
  box-sizing: border-box;
}

h1 {
  color: white;
  font-size: 50px;
  text-align: center;
  padding-top: 80px;
  font-weight: 600;
}

.cards {
  display: flex;
  justify-content: space-between;
  gap: 15px;
  padding: 30px;
}

.card {
  background-color: white;
  border-radius: 10px;
  box-shadow: 5 5 black;
  flex: 1;
  display: flex;
  flex-direction: column;
  padding: 10px;
  height: 400px;
  position: relative;
}

.card img {
  width: 100%;
  height: 140px;
  box-sizing: border-box;
  object-fit: cover;
  object-position: top;
  border-radius: 10px;
}

h2 {
  font-size: 20px;
  font-weight: bold;
  margin-top: 20px;
  margin-bottom: 10px;
}

p {
  margin-bottom: 5px;
  line-height: 20px;
}

svg {
  color: grey;
  font-size: 20px;
  position: absolute;
  bottom: 10px;
  right: 10px;
}

@media (max-width: 960px) {
  .cards {
    flex-direction: column;
    align-items: center;
  }

  .card {
    width: 300px;
  }
}
</style>
