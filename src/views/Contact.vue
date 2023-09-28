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
                            <label for="company">メールアドレス<span> *</span></label>
                            <input type="mail" id="company" name="" required>
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
#contact {
    height: 100vh;
    background: url("../assets/images/contact.jpg");
    background-position: center;
    background-size: cover;
    background-attachment: fixed;

    h1 {
        font-size: 1.8rem;
        color: white;
        text-align: center;
    }
}

form {
  width: 100%;
  max-width: 600px;
  margin: 0 auto;

  .row {
    display: flex;
    justify-content: space-between;

    .col {
      flex: 1;

      &:not(:last-child) {
        margin-right: 10px; // Adjust the gap between columns
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
          border: 1px solid #ccc;
          border-radius: 4px;
          background-color: #f9f9f9;
          font-size: 16px;
        }

        input[type="text"]:required,
        input[type="email"]:required {
          background-color: #f9f9f9; // Change background color for required fields
        }
      }
    }
  }

  textarea {
    width: 100%;
    padding: 10px;
    box-sizing: border-box;
    border: 1px solid #ccc;
    border-radius: 4px;
    background-color: #f9f9f9;
    font-size: 16px;
    margin-bottom: 15px;
    resize: vertical;
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