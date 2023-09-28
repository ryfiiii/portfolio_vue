<template>
    <div>
        <header>
            <nav>
                <ul>
                    <li>Profile</li>
                    <li>Skill</li>
                    <li>Creation</li>
                    <li>Contact</li>
                </ul>
            </nav>
        </header>
    </div>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
header {
    width: 100%;
    position: absolute;

    nav {
        display: flex;
        justify-content: end;
        align-items: center;
        height: 60px;

        ul {
            display: flex;
            justify-content: center;
            align-items: center;

            li {
                list-style: none;
                margin-right: 10px;

                &:last-child {
                    margin-right: 80px;
                }
            }
        }
    }
}
</style>