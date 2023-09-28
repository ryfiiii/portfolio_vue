<template>
    <div>
        <header>
            <nav>
                <ul>
                    <li><a href="#profile">Profile</a></li>
                    <li><a href="#skill">Skill</a></li>
                    <li><a href="#creation">Creation</a></li>
                    <li><a href="#contact">Contact</a></li>
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

                &:last-child {
                    margin-right: 60px;
                }

                a {
                    text-decoration: none;
                    padding: 12px 15px;

                    &:hover {
                        background-color: #ffffff6e;
                    }
                }
            }
        }
    }
}
</style>