<template>
  <section class="about-container">
    <h1>Sobre esta aplicação</h1>
    <p> To-Do or no To-Do é uma aplicação de checklist feita para facilitar
    a organização de tarefas dos nossos usuários. Pode ser estudo, assuntos pessoais,
    trabalho, exercício ou qualquer outra coisa, basta escrever, adicionar a tarefa e 
    voila! Sua checklist está pronta!</p>
    <h1>Como utilizar</h1>
    <p>Na página principal, escreva sua tarefa na caixa de texto, e em seguida,
    clique em <span class="add-button">Criar</span>, sua tarefa irá aparecer
    na lista de tarefas pendentes!, caso tenha terminado, simplesmente clique
    em <input type="checkbox"> para riscá-la. Caso precise escluir sua tarefa,
    clique no botão <span class="remove-button">Excluir</span> e prontinho!</p>
  </section>
</template>

<script>
export default {
  data () {
    return { }
  }
}
</script>

<style>

    .about-container {
        width: 60%;
        margin: 0 auto;
    }

    .about-container h1 {
        margin: 40px 0 20px 0;
        font-size: 24px;
        color: #e65a2f;
    }

    .about-container p {
        text-align: justify;
        text-indent: 2em;
        line-height: 2em;
        margin-bottom: 20px;
    }

    .add-button {
        border-radius: 5px;
        background-color: #1cc438;
        border: none;
        color: white;
        height: 30px;
        padding: 5px 10px;
    }

    .remove-button {
        border-radius: 5px;
        background-color: #e22525;
        color: white;
        border: none;
        height: 30px;
        padding: 5px 10px;
    }

</style>
