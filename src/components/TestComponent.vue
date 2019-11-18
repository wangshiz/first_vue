<template>
  <div class="hello">
    接受到的数据:{{msg}}
    <button @click="getList">获得数据</button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Hello',
  data () {
    return {
      msg: ''
    }
  },
  methods: {
    getList () {
      axios.get('https://api.coindesk.com/v1/bpi/currentprice.json').then(response => {
        this.msg = response
      }).catch(error => console.log(error))

      // var request = {
      //   method: 'post',
      //   url: '/user',
      //   data: {firstName: 'Fred', lastName: 'Flintstone'}
      // }
      // axios(request).then(response => (this.msg = response))
      //   .catch(error => {
      //     console.log(error)
      //   })

      // var instance = axios.create({
      //   baseURL: 'https://www.baidu.com'
      // })
      // var request = {
      //   method: 'get',
      //   url: '/s',
      //   params: {wd: 'vue'}
      // }
      // // 当传入了url参数的时候，才会发起请求，所以虽然都是传配置，但上面的那个并没有发起请求
      // instance(request)
      //   .then(response => {
      //     console.log(response)
      //   })
      //   .catch(error => {
      //     console.log(error)
      //   })
    }
  }
}

</script>
