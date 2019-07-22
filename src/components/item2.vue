<template>
    <div>
        <p class="paragraph">{{msg}}</p>
    </div>
</template>

<script>
export default {
name: "item2",
props: {
    msg: String
}

}
</script>

<style scoped>
 .paragraph {
     border: pink 1px solid;
     color: navy;
     background: yellow;
     height: 30px;
 }
</style>
