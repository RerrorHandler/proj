<template>
    <div class="Content">
        <div class="Contact">
            <div class="ContactConteiner" v-for="(user, i) in users" :key="i">
                <div class="Avatar"></div>
                <div class="Name">{{users}}</div>
            </div>
        </div>
        <div class="Chat">

        </div>
    </div>
</template>

<script>
export default {
  name: 'Name',
  props: {
    uesrs: Array
  }
}
</script>

<style scoped>
.Content {
    display: flex;
    width: 100%;
    height: 100%;
    background: white;
    flex-direction: row;
}
.Content .Contact {
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 200px;
    background-color: #f1f1f1;
    border: 1px solid #f6f2f260;
}
.Content .Contact .Avatar {
    width: 40px;
    height: 40px;
    border: 1px solid transparent;
    border-radius: 25px;
    background-color: #a0c5e8;
}
.Content .Contact .ContactConteiner {
    padding: 5px 5px;
}
</style>
