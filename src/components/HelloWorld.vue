<template>
 <table>
        <thead>
              <tr>
                <th>Block Height</th>
                <th>Block Hash</th>
                <th>Previous Hash</th>
                <th>Timestamp</th>
                <th>Transactions</th>
              </tr>
         </thead>
            <tbody>
              <tr v-for="alias in chainData" id="tRow" :key="alias.index">
                <td>{{alias.index}}</td>
                <td>{{alias.hash}}</td>
                <td>{{alias.prevHash}}</td>
                <td>{{alias.timestamp}}</td>
                <td>{{alias.transactions}}</td>
              </tr>
            </tbody>
          </table>
</template>

<script>
import iotapp from "iotapp-api" //Linked NPM module

export default {
data () {
    return {
      chainData: [],
    }
}, 
methods: {

},

  mounted() {
// Pass app key(s) as argument.
iotapp.getPrivateChain("YOUR_IOTAPP_API_KEY(S)")
  .then(data => this.chainData = data)
  .catch(err => console.log("Error occurred:", err))
  },
}
</script>
