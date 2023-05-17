<template>
    <div>
        <List-item class="card" v-for="(item, index) in items"
        :key="index"
        :listItemTitle="item.title"
        :cardFillText="item.text"
        :index="index"
        >
        {{item.title}}
        {{item.text}}
    </List-item>
    </div>
</template>

<style scoped>
.card{
    background-color: #f8f8f8;
    border-radius: 4px;
    padding: 50px;
    margin-bottom: 10px;
    margin-right: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h1{
    font-size: 18px;
    margin-bottom: 5px;
}

p{
    font-size: 14px;
    color: #555555;
}
</style>

<script>
export default {
    data() {
        return{
            items: [
                {title:'Title 1',text:'text 1'},
                {title:'Title 2',text:'text 2'},
                {title:'Title 3',text:'text 3'},
            ]
        };
    }
}
</script>