<template>
    <section id="contact">
        <h1>Contact</h1>
        <div class="form">
            <form action="https://formspree.io/f/xaygjdpp" method="POST">
                <div class="row">
                    <div class="col">
                        <div class="form-group">
                            <label for="sei">姓<span> *</span></label>
                            <input type="text" id="sei" name="first_name" required>
                        </div>
                    </div>
                    <div class="col">
                        <div class="form-group">
                            <label for="mei">名<span> *</span></label>
                            <input type="text" id="mei" name="last_name" required>
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <div class="form-group">
                            <label for="company">会社名</label>
                            <input type="text" id="company" name="company">
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <div class="form-group">
                            <label for="mail">メールアドレス<span> *</span></label>
                            <input type="mail" id="mail" name="email" required>
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <div class="form-group">
                            <label for="contents">内容<span> *</span></label>
                            <textarea name="contents" id="contents"></textarea>
                        </div>
                    </div>
                </div>

                <div class="btn-container">
                    <input type="submit" value="送信">
                </div>
            </form>
        </div>
    </section>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";

#contact {
    width: 100%;
    height: 100%;
    padding: 50px 0 80px 0;
    @include flexCenter;
    flex-direction: column;
    background: url("../assets/images/contact.jpg");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    @include mq(){
        background-attachment: scroll;
    }

    h1 {
        font-size: 1.8rem;
        color: white;
        text-align: center;
        margin-bottom: 30px;
    }
}

form {
    background-color: #ccc;
    width: 100%;
    max-width: 1000px;
    padding: 70px 80px;
    margin: auto;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.3);


    .row {
        display: flex;
        justify-content: space-between;

        .col {
            flex: 1;

            &:not(:last-child) {
                margin-right: 10px;
            }

            .form-group {
                margin-bottom: 15px;

                label {
                    display: block;
                    margin-bottom: 5px;
                    font-weight: bold;

                    span {
                        color: red;
                    }
                }

                input {
                    width: 100%;
                    padding: 10px;
                    box-sizing: border-box;
                    border-radius: 8px;
                    background-color: #f9f9f9;
                    font-size: 16px;
                    outline: none;
                    border: 3px solid #ccc;

                    &:focus {
                        border: 3px solid rgb(97, 97, 255);
                    }
                }
            }
        }
    }

    textarea {
        width: 100%;
        height: 150px;
        padding: 10px;
        box-sizing: border-box;
        border: 3px solid #ccc;
        border-radius: 8px;
        background-color: #f9f9f9;
        font-size: 16px;
        margin-bottom: 15px;
        resize: vertical;
        outline: none;

        &:focus {
            border: 3px solid blue;
        }
    }

    .btn-container {
        display: flex;
        justify-content: center;

        input[type="submit"] {
            background-color: #007bff;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;

            &:hover {
                background-color: #0056b3;
            }
        }
    }
}
</style>