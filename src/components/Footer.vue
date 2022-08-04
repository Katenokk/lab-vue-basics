<template>
 <div>
 <ul :class="flex">
    <li>
        <a href="#" :class="ancor">Contact Us</a>
    </li>
    <li>
        <a href="/about" :class="ancor">About Us</a>
    </li>
    <li>
        <a href="#" :class="ancor">Some stuff</a>
    </li>
 </ul>
 </div>
</template>

<script>
export default {
    data() {
        return {
            flex: {
                class: "link"
            },
            ancor: {
                class: "none"
            }
        }
    }
}
</script>

<style>
.link {
    display: flex;
}
.none {
    list-style: none; /*me estoy mareando*/
}


</style>
