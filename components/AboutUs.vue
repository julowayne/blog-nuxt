<template>
  <div class="signin flex grid-cols-2 text-center m-0">
    <div id="content">
      <div id="about">
        <img class="shadow" src="https://media.giphy.com/media/OVXDh4cOaLawM/giphy.gif" alt="">
        <h2 class="text-2xl p-3">
          About us:
        </h2>
        <p class="p-5 text-left">
          We provide the lastest news about whatever you might want to know.
        </p>
      </div>
      <div>
        <form class="bg-white shadow-md">
          <h1>Tell us what content you want</h1>
          <div class="mb-3">
            <label class="block" for="name">
              Lastname
            </label>
            <input id="name" class="w-full h-8 shadow border rounded focus:outline-none focus:ring-1 focus:ring-green-300 focus:border-transparent" type="text">
          </div>
          <div class="mb-3">
            <label class="block" for="firstname">
              Firstname
            </label>
            <input id="firstname" class="w-full h-8 shadow border rounded focus:outline-none focus:ring-1 focus:ring-green-300 focus:border-transparent" type="text">
          </div>
          <div class="mb-3">
            <label class="block" for="email">
              Email
            </label>
            <input id="email" class="w-full h-8 shadow border rounded focus:outline-none focus:ring-1 focus:ring-green-300 focus:border-transparent" type="text">
          </div>
          <div class="mb-3">
            <label class="block" for="objet">
              Object
            </label>
            <input id="objet" class="w-full h-8 shadow border rounded focus:outline-none focus:ring-1 focus:ring-green-300 focus:border-transparent" type="text">
          </div>
          <div class="mb-3">
            <label class="block" for="password">
              Message
            </label>
            <textarea id="message" class="w-full shadow border rounded focus:outline-none focus:ring-1 focus:ring-green-300 focus:border-transparent" name="message" cols="35" rows="2" />
          </div>
          <div id="send" class="flex items-center">
            <button class="shadow text-white font-bold rounded hover:shadow-xl transition-shadow duration-200 ease-in-out" type="button">
              Send
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>

body {
    background-color: #e9ecef;
}
h2 {
  text-align: left;
  color: #007bff;
}
#about {
  background-color: white;
}
.signin {
  display: flex;
  height: 85vh;
  width: 100%;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
  margin-top: 2em;
}
#content {
    max-width: 800px;
    overflow: hidden;
    display: flex;
    justify-content: center;
    border-radius: 4px;
    box-shadow: 0 .5rem 1rem rgba(0,0,0,.15)!important;
  }
  #logo {
    width: 400px;
    background-color: #007bff;
  }
  img {
    width: 100%;
  }
  form {
      width: 400px;
      height: 100%;
      text-align: left;
      padding: 1rem 2rem;
      background-color: white;
    }
  h1 {
    margin-bottom: 1rem;
    font-size: 2rem;
    border-bottom: 1px solid #007bff;
    padding: 1rem 0;
    letter-spacing: 0.5px;
    color: #007bff;
  }
  #send {
    margin: 1.5rem 0 1rem;
    text-align: right;
  }
  button {
    width: 100%;
    height: 2.5rem;
    background-color: #007bff;
  }

</style>
