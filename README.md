## SEI atlantic-1 keplr wallet integration
<!--
#### Requirements 
[keplr wallet extension](https://google.com)
-->
### Auto installation
1) Just visit this link. Once the keplr window popup press the approve button.  
2) In the network section choose SEI atlantic-1 network  
3) That's it. Have fun:)  

### Manual installation

Open the developer console:

- Chromium based browsers: View> Developer>Developer Tools(ctrl-shift-j)

- Copy paste the code and press enter. Do not forget to edit rpc and rest api urls in the code! :


```markdown
await window.keplr.experimentalSuggestChain({
    chainId: "atlantic-1",
    chainName: "SEI",
    rpc: "http://78.107.234.44:16657", // replace with your rpc url
    rest: "http://78.107.234.44:1317", // replace with your rest api url
    bip44: {
        coinType: 118,
    },
    bech32Config: {
        bech32PrefixAccAddr: "sei",
        bech32PrefixAccPub: "sei" + "pub",
        bech32PrefixValAddr: "sei" + "valoper",
        bech32PrefixValPub: "sei" + "valoperpub",
        bech32PrefixConsAddr: "sei" + "valcons",
        bech32PrefixConsPub: "sei" + "valconspub",
    },
    currencies: [ 
        { 
            coinDenom: "SEI", 
            coinMinimalDenom: "usei", 
            coinDecimals: 6, 
            coinGeckoId: "usei", 
        }, 
    ],
    feeCurrencies: [
        {
            coinDenom: "SEI",
            coinMinimalDenom: "usei",
            coinDecimals: 6,
            coinGeckoId: "usei",
        },
    ],
    stakeCurrency: {
        coinDenom: "SEI",
        coinMinimalDenom: "usei",
        coinDecimals: 6,
        coinGeckoId: "usei",
      },
    coinType: 118,
    gasPriceStep: {
        low: 0.01,
        average: 0.025,
        high: 0.03,
    },
    
  
});
}
```
