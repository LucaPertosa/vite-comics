<script>
export default {
    name: "AppMain",
    data() {
        return {
        
        }
    }
}
</script>

<template>
    <main>
        <p>
            
        </p>
    </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
@use "../style/general.scss" as *;

main {
    background-color: black;
    color: white;
}
p {
    margin: 0 auto;
    padding: 50px 0;
    width: $width;
}
</style>