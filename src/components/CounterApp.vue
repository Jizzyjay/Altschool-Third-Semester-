<template>
  <div class="counterContainer">
    <h2 class="heading-main">Current Count: {{ count }}</h2>

    <div class="input-wrapper">
      <input class="input-field" type="number" v-model="value" />
      <input
        class="submit"
        type="submit"
        @click="setValue(value)"
        value="Set Value"
      />
    </div>
    <div class="btn-wrapper">
      <button class="btn decrement" @click="decrement">Decrement</button>
      <button class="btn increment" @click="increment">Increment</button>
    </div>
    <button class="btn reset" @click="reset">Reset</button>
  </div>
</template>

<script>
import useCounter from "@/composables/counterfunc";

export default {
  setup() {
    const { count, increment, decrement, reset, setValue } = useCounter();

    return {
      count,
      increment,
      decrement,
      reset,
      setValue,
      value: 0,
    };
  },
};
</script>

<style scoped>
.counterContainer {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 100vw;
  margin: 0 auto;
  height: calc(100vh - 60px);
  flex-direction: column;
}
.heading-main {
  font-size: 48px;
  margin-bottom: 16px;
  text-align: center;
  font-family: "Libre Baskerville", serif;
  font-weight: bolder;
}
.btn-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 4rem;
  margin: 2rem;
}
.btn {
  width: 140px;
  height: 55px;
  font-size: 1rem;
  font-family: "Libre Baskerville", serif;
  outline: none;
  border: none;
  border-radius: .6rem;
  color: black;
}
.btn.reset {
  background-color: #282c34;
  color: #fff;
}
.btn.reset:hover {
  background-color: #3f497f;
  border: 1px solid #000;
  color: #fff;
  transition: all 0.4s;
  cursor: pointer;
}
.btn.increment {
  background-color: #37cf71;
  color: #fff;
}
.btn.increment:hover {
  background-color: #3f497f;
  border: 1px solid #6568f4;
  color: #fff;
  cursor: pointer;
}
.btn.decrement {
  background-color: red;
  color: #fff;
}
.btn.decrement:hover {
  background-color: #3f497f;
  border: 1px solid red;
  color: #fff;
  font-weight: bolder;
  transition: all 0.4s;
  cursor: pointer;
}
.input-wrapper {
  width: 98%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
input {
  height: 50px;
  padding: 10px;
  width: 300px;
  margin: 20px 0 20px 0;
  font-family: "Libre Baskerville", serif;
  font-size: 1rem;
}
.input-field {
  border-radius: 10px 0 0 10px;
  outline: none;
}

.submit {
  border-radius: 0 10px 10px 0;
  background-color: red;
  color: #fff;
  width: 100px;
  font-weight: bolder;
  font-size: 1rem;
  font-family: "Libre Baskerville", serif;
  outline: none;
  border: none;
}
.submit:hover {
  background-color: #3f497f;
  color: #fff;
  border: 1px solid #3f497f;
  transition: all 0.4s;
  cursor: pointer;
}
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
