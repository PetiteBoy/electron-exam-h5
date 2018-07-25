<template>
  <div id="wrapper">
    <video id="video"></video>
  </div>
</template>

<script>
export default {
  name: 'landing-page',
  data () {
    return {}
  },
  mounted () {
    this.video()
  },
  methods: {
    video () {
      navigator.mediaDevices
        .getUserMedia()
        .then(stream => {
          console.log(stream)
          /* 使用这个stream stream */
        })
        .catch(err => {
          console.log(err)
          /* 处理error */
        })
    }
  }
}
</script>
