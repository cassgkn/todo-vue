<script setup>

    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])

</script>


<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                    type="text" placeholder="Digite a descrição da tarefa" class="form-control">
            </div>
            <div class="col-md-1">
                <button class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocarFiltro" class="form-control bg-warning">
                    <option value="todas" class="text-center">Todas tarefas</option>
                    <option value="pendentes" class="text-center">Pendentes</option>
                    <option value="finalizadas" class="text-center">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>