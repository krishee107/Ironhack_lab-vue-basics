<template>
    <div class="container">
        <div class="post" v-for="element in data">
        <div class="title">{{element.title}}</div>
        <div class="description">{{element.description}}</div>
        <div class="content">{{element.content}}</div>
    </div>

    </div>

</template>
<script setup >
    const data = [
        {
            title: "Titulo1",
            description: "random desc",
            content: "Content lorem ipsum"
        },
        {
            title: "Titulo2",
            description: "random desc2",
            content: "Content lorem ipsum2"
        },
        {
            title: "Titulo3",
            description: "random desc3",
            content: "Content lorem ipsum3"
        },
        {
            title: "Titulo4",
            description: "random desc4",
            content: "Content lorem ipsum4"
        },
        {
            title: "Titulo5",
            description: "random desc5",
            content: "Content lorem ipsum5"
        },
        {
            title: "Titulo6",
            description: "random desc6",
            content: "Content lorem ipsum6"
        },
    ]
</script>
<style scoped>
.container{
    display: flex;
    flex-wrap: wrap;
    gap: 24px;
}
.post{
    box-shadow: 6px 5px 10px 3px #dadada;
    width: 300px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding: 10px;
    border-radius: 25px;
}
.title{
    font-size: 30px;
    font-weight: bold;
}
.content{
    font-size: 20px;
}
</style>