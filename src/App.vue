<script setup></script>

<template>
  <header>
    <h1>Todos</h1>
  </header>
  <main>
    <div class="add-todo-container">
      <input type="text" placeholder="New Todo" />
      <button type="button">+</button>
    </div>
    <div class="todos-list-container">
      <ul class="todos">
        <li>
          <input type="checkbox" id="done" />
          <span id="todo-name">Take out trash</span>
          <button type="button" id="delete">X</button>
        </li>
        <li>
          <input type="checkbox" id="done" />
          <span id="todo-name">Take out trash</span>
          <button type="button" id="delete">X</button>
        </li>
        <li>
          <input type="checkbox" id="done" />
          <span id="todo-name">Take out trash</span>
          <button type="button" id="delete">X</button>
        </li>
        <li>
          <input type="checkbox" id="done" />
          <span id="todo-name">Take out trash</span>
          <button type="button" id="delete">X</button>
        </li>
      </ul>
    </div>
    <div class="completed-todos-container"></div>
  </main>
</template>

<style scoped>
header {
  display: flex;
  width: 100%;
  justify-content: center;
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2rem;
  color: var(--columbia-blue);
}
#todo-name {
  cursor: default;
}

.add-todo-container {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 2rem;
}
.todos-list-container {
  margin-top: 4rem;
  width: 100%;
}
ul.todos {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  padding: 0;
}
li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style: none;
  gap: 3rem;
  border: 1px solid var(--columbia-blue);
  color: var(--columbia-blue);
  padding: 0.75rem;
  border-radius: 5px;
}
li:hover {
  background-color: var(--columbia-blue);
  color: var(--steel-blue);
}
input#done {
  cursor: pointer;
  height: 1.5rem;
  width: 1.5rem;
  border: 1px solid red;
  border-radius: 5px;
}
button#delete {
  background: red;
  border: 1px solid red;
  color: white;
  font-weight: 600;
  cursor: pointer;
  font-size: 1rem;
  height: 1.75rem;
  width: 1.75rem;
  border-radius: 5px;
}
button#delete:hover {
  box-shadow: 0 0 5px 0 var(--color-background);
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
