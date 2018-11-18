<template>
  <section class="todo-container">
    <div class="create-task-container">
      <input 
        v-model="newTask"
        type="text"
        @keyup.13="addTask()">
      <button @click="addTask()">
        <span>Criar</span>
      </button>
    </div>
    <div class="task-list-container">
      <div class="list-title">Tarefas</div>
      <ul class="task-list">
        <li 
          v-for="task in tasks" 
          :key="task.task"
          class="task-list-item">
          <input
            v-model="task.done"
            type="checkbox">
          <p 
            :class="{ done: task.done }"
            class="task-title">
            {{ task.task }}</p>
          <button
            @click="removeTask(task)">
            <span>Excluir</span>
          </button>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>

export default {
  data () {
    return {
      newTask: '',
      tasks: [
        { task: "Pegar a filha no balé", done: false },
        { task: "Fazer compras do mês", done: false },
        { task: "Inscrever as crianças na aula de teatro", done: true }
      ]
    }
  },
  methods: {
    addTask () {
      if (this.newTask != '') {
        this.tasks.push(
          { task: this.newTask }
        );

        this.newTask = '';
        }
    },

    removeTask (task) {
      let index = this.tasks.indexOf(task);
      this.tasks.splice(index, 1);
    }
  }
}
</script>

<style>

  button {
    cursor: pointer;
  }

  .todo-container {
      margin: 0 auto;
      max-width: 650px;
      display: flex;
      margin-top: 40px;
      justify-content: center;
      flex-direction: column;
  }

  .create-task-container {
      width: 100%;
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
  }

  .create-task-container input {
      width: 80%;
      border-radius: 5px;
      border: 1px solid lightgray;
      padding: 5px 10px;
  }

  .create-task-container button {
      width: 15%;
      border-radius: 5px;
      background-color: #1cc438;
      border: none;
      height: 30px;
      padding: 5px 10px;
  }

  .list-title {
    background-color: #e65a2f;
    color: white;
    padding: 10px; 
    font-size: 18px;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
  }

  .task-list-container {
    margin-bottom: 40px;
  }

  .task-list-container button {
      width: 15%;
      border-radius: 5px;
      background-color: #e22525;
      border: none;
      height: 30px;
      padding: 5px 10px;
  }

  button span {
      color: white;
      font-family: 'Roboto Condensed', sans-serif;
      font-size: 15px;
  }

  .create-task-container button:hover {
      background-image: url(/icons/happy.svg);
      background-size: 25px;
      background-repeat: no-repeat;
      background-position: center;
      background-color: #2dbe45;
  }

  .task-list-container button:hover {
      background-image: url(/icons/surprise.svg);
      background-size: 25px;
      background-repeat: no-repeat;
      background-position: center;
      background-color: #c51e1e;
  }

  button:hover span {
      display: none;
  }

  .task-list {
      border: 1px solid lightgray;
      padding: 20px;
      border-bottom-left-radius: 5px;
      border-bottom-right-radius: 5px;
  }

  .task-list-item {
    display: flex;
    align-items: center;
    border-bottom: 1px dashed lightgray;
  }

  .task-list-item:last-child {
    border-bottom: none;
  }

  .task-title {
      width: 95%;
      margin: 15px 5px;
  }

  .done {
      text-decoration-line: line-through;
      color: gray;
  }

</style>
