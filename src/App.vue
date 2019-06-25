<template>

<div id="" >

<nav class="navbar is-transparent">
  <div class="navbar-brand">
    <a class="navbar-item" :href="cleanUrl">
      <img src="data:image/png;base64,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" alt="TweetWeave" width="112" height="28">
    </a>
    <div class="navbar-burger burger" data-target="navbarExampleTransparentExample">
      <span></span>
      <span></span>
      <span></span>
    </div>
  </div>

  <div id="navbarExampleTransparentExample" class="navbar-menu">
   
    <div class="navbar-end">
      <div class="navbar-item">
        <div class="field is-grouped">
         
          <p class="control">
            <span >Swap Pool Balance:  <b class="has-text-primary">{{Math.trunc(arSwapPoolBalance)}} AR </b></span> &nbsp;
            <span>ETH-USD : <b class="has-text-primary">${{ethUsd}}</b></span> &nbsp;
            <span>AR-USD : <b class="has-text-primary">${{arUsd}}</b></span> &nbsp;&nbsp;&nbsp;&nbsp;
            
          </p>
        </div>
      </div>
    </div>
  </div>
</nav>

    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <div class="columns" id="app">
            <div class="column is-three-fifths is-offset-one-fifth">

                <section v-if="arTxnView">
                <b-notification type="is-success" :active.sync="arViewTxnId" aria-close-label="notification">
                  Swap txn <a :href="'https://viewblock.io/arweave/tx/'+this.arViewTxnId">{{this.arViewTxnId}}</a> is  confirmed in Arweave.<br/>
                </b-notification>
                <b-notification v-if="arViewTxnId == false" aria-close-label="notification">
                  Swap txn is not confirmed in Arweave. Please wait for a while and check back later<br/>
                </b-notification>

                <br/><br/>
                <a :href="cleanUrl">
                  <b-button size="is-medium" type="is-primary" outlined>Create a new swap
                  </b-button>
                </a>

              </section>

             
            
          <section v-if="!arTxnView" > 

            <b-notification
                type="is-danger"
                aria-close-label="Close notification"
                role="alert" v-if="!web3js" >
                <span style="text-align:center"> 
                  Not connected any web3 providers. Please connect to mainnet via metamask</span>
            </b-notification>

         
              <h2 class="subtitle">
                Enter Arweave address for reciving AR after swap (ETH - AR)
              </h2>

              <b-field label="">
               <b-input v-model="arAddr" placeholder="AR Address" required></b-input>
             </b-field> <br/>


              <div class="field has-addons has-addons-centered">
                <p class="control">
                  <span class="select">
                    <select>
                      <option>AR</option>
                      <!-- <option>£</option>
                      <option>€</option> -->
                    </select>
                  </span>
                </p>
                <p class="control">
                  <input class="input" type="number" min="1" v-model="arCount" placeholder="Amount of AR" required>
                </p>
                <p class="control">
                  <a class="button is-primary" @click="confirmSwap()">
                    Swap
                  </a>
                </p>
              </div>
              <div class="field has-addons has-addons-centered">  
                <span>ETH : {{ethAmount.toFixed(5)}}</span>
              </div>  


               <b-notification aria-close-label="Close notification" v-if="swapEthTxn" >
                 ETH <a :href="'https://etherscan.io/tx/'+swapEthTxn" target="_blank">transaction</a> is sent. Please wait for a few AR blocks to pass, it will take a little while for processing swap.
               </b-notification>


          </section>

           <div class="container"> 

            <div class="columns">
              <div class="column is-three-fifths is-offset-one-fifth">
                <section  v-if="Object.keys(arTxnData).length">
                      <hr>
                      <b-table  :data="arTxnData" :columns="arTxnColumns"></b-table>

                </section>
              </div>
            </div>       
        
          </div>

          <br/><br/>


       </div>
      </div>     

          
        </div>
      </div>
    </section>



  </div>
</template>

<script>

import Web3 from 'web3';
import Arweave from 'arweave/web';

const arweave = Arweave.init({
  host: 'arweave.net', 
  port: 1984, 
  protocol: 'https'
  });


export default {
  name: 'app',
  data: function () {
    return {
      ethAddr: '0xcE4C9AdA8C807FDd84D78598bd52D780796D837D',
      ethTxns: null,
      ethUsd: null,
      arAddr: '',
      arUsd: 1.0,
      arCount: 0,
      arTxns: null,
      arSwapPoolAddr: 'ZFRzSlS_9tzMFmDvvQNHvOCrcOUhI2ejFpuUEWVXoKU',
      arSwapPoolBalance: 0.0,
      web3js: false,
      arTxnColumns: [   
                    {
                        field: 'txn_id',
                        label: 'Your Swap Transactions in Arweave ',
                        renderHtml: true
                    },       
                ],
      arTxnData: [ 
      ],
      arTxnView: false,
      arViewTxnId: false,
      swapEthTxn: false


    }
  },    
  created: function(){

    this.getPrices()
    this.getSwapPoolBalance()
    this.loadWeb3()
    //this.getEthTxns()
    this.getArSwapTxns()


    const urlParams = new URLSearchParams(window.location.search);
    const txn = urlParams.get('txn');

    if(txn != '' && txn != null)   {
      this.arTxnView = true
      this.checkSwapStatus(txn)
      
    }  

  },
  methods:  {

    confirmSwap() {

      if(this.arAddr == null || this.arAddr ==  '' || this.arCount == 0) {
        return;
      }

       this.$dialog.confirm({
            message: 'Are you sure about this? <br/> Please double check the AR address you provided <b>'+ this.arAddr+'</b>',
            onConfirm: () => {
              this.swap()
            } 
        })

    },

    async swap() {

      if(this.arAddr == null || this.arCount == 0) {
        return;
      }
      let account = web3.eth.accounts[0]
      if(!account) {
        this.$dialog.alert('Please Unlock Metamask.')
        return
      }



      if(parseInt(this.arSwapPoolBalance) <= this.arCount) {
        this.$dialog.alert('Sorry, not enough AR available in the swap pool.')
        return;
      }
        
      console.log(web3.eth.accounts[0]) 
      //web3.eth.getBalance(web3.eth.accounts[0]).then(console.log);

      let balance = await this.getBalance()

      let amount = this.arCount *  (this.arUsd / this.ethUsd)

      let $this = this
      

      web3.eth.getAccounts(function(error, result) { 
        web3.eth.sendTransaction(
            {from:web3.eth.accounts[0],
            to: $this.ethAddr,
            value:  web3.toWei(amount.toFixed(5), 'ether'), 
            gasPrice: web3.toWei('5', 'gwei'),
            gas: 100000,
            data: web3.toHex('AR_5EN4sYqRlw0yKdR3lpBlZWHvfo520T0u1SNhwSJmG4g')
                }, function(err, transactionHash) {
          if (!err) {
            console.log(transactionHash + " success" + $this.arUsd); 
            $this.swapEthTxn = transactionHash
          }  
        });
    });

    },

    async getSwapPoolBalance() {

       arweave.wallets.getBalance(this.arSwapPoolAddr).then((balance) => {
          console.log('balance :' + arweave.ar.winstonToAr(balance))
          this.arSwapPoolBalance = arweave.ar.winstonToAr(balance)
          })

    },

    getEthTxns() {

      this.$axios.get('http://api.etherscan.io/api?module=account&action=txlist&address='+ this.ethAddr+'&startblock=0&endblock=99999999&sort=desc&apikey=', {
        })
        .then(res => { 
          console.log(res.data.result)

          this.ethTxns = res.data.result
              
        }).catch(err => { 
          
            console.log(err)
        })


    },

    async getArSwapTxns() { 

       const txIds = await arweave.arql({
              op: "and",
              expr1: {
                op: "equals",
                expr1: "from",
                expr2: this.arAddr
              },
              expr2: {
                op: "equals",
                  expr1: "txn-eth-addr",
                  expr2: web3.eth.accounts[0]
                
              }
        })

        txIds.forEach(tx_id => {
          this.arTxnData.unshift({txn_id: '<a href="https://viewblock.io/arweave/tx/'+ tx_id +'"  target="_blank"> '+tx_id+'</a>'
                        
          })
          
        }); 

        //console.log(txIds)

    },

    async checkSwapStatus(txn) { 

       const txIds = await arweave.arql({
              op: "and",
              expr1: {
                op: "equals",
                expr1: "from",
                expr2: this.arAddr
              },
              expr2: {
                op: "equals",
                  expr1: "txn-eth-hash",
                  expr2: txn
                
              }
        })

       if(txIds.length)  {

          this.arViewTxnId = txIds[0]
         console.log('Txn found ')

       }else {

         console.log('Txn not found')
       }
        
       // console.log(txIds)

    },

    getPrices() { 

       this.$axios.get('https://api.etherscan.io/api?module=stats&action=ethprice&apikey=VJJRWC92NA99GVCK8HI8PK99GK4314MXJK', {
        })
        .then(res => { 

          this.ethUsd = res.data.result.ethusd
              
        }).catch(err => { 
          
            console.log(err)
        })

    },
     async getBalance() {

          web3.eth.getBalance(web3.eth.accounts[0], function(error, result){
          if(!error) { 
              return result 
          }
          else
              console.error(error);
        })

    },
    loadWeb3() {

      let $this = this

      window.addEventListener('load', function() {
        let web3js

        // Checking if Web3 has been injected by the browser (Mist/MetaMask)
        if (typeof web3 !== 'undefined') { 
          // Use Mist/MetaMask's provider
          web3js = new Web3(web3.currentProvider);
          $this.web3js = true

        } else {
          console.log('No web3? You should consider trying MetaMask!')
          // fallback - use your fallback strategy (local node / hosted node + in-dapp id mgmt / fail)
          //web3js = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
        }


      })


    }

  },
  computed: {
    cleanUrl: function () {
      return [location.protocol, '//', location.host, location.pathname].join('');
    },
    ethAmount: function() {
            return  this.arCount *  (this.arUsd / this.ethUsd)
    }
  },
  components: {
    // HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
