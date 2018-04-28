<template>
  <div>
    Hello My Components
    {{ msg }}
    <button @click="myFunc(msg)">Hi</button>
    <button @click="myFunct()">Hisss</button>
  </div>
</template>

<script>
export default {
  props: {
    msg: {
      type: String
    },
    myFunc: {
      type: Function
    },
    myFunct: {
      type: Function
    }
  }
}
</script>