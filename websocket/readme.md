### Base Websocket URI
```
wss://api-rs.dexcelerate.com/ws
```
### Required headers
```
headers = {
    "Origin": "https://app.dexcelerate.com"
}
```
<br></br>

# Broadcast messages
### These are sent without subscribing to anything
### Price updates
```
{
    "data": {
        "prices": {
            "BASE": "3126.64458500",
            "BSC": "677.26551500",
            "ETH": "3130.59425000",
            "SOL": "230.39893000"
        }
    },
    "event": "wpeg-prices"
}
```
<br></br>

# Subscribe to token pair updates
### Request json
```
{
    "event": "subscribe-pair-stats",
    "data": {
        "pair": "CsVe97sDiaXkVfVjiwyYp4zKZXD7TckaRcLVgqbFuUay",
        "token": "6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN",
        "chain": "SOL",
        "routerType": "RAYDIUM_CLMM"
    }
}
```
### Response json
```

{
    "data": {
        "callCount": 14,
        "migrationProgress": null,
        "pair": {
            "burnedSupply": "0",
            "chain": "SOL",
            "fdv": "26985221716.52469898824932",
            "freezeAuthorityRenounced": true,
            "isVerified": true,
            "linkTwitter": "https://x.com/ecashonsolana",
            "mintAuthorityRenounced": true,
            "pairAddress": "CsVe97sDiaXkVfVjiwyYp4zKZXD7TckaRcLVgqbFuUay",
            "pairCreatedAt": "2025-01-18T02:07:36Z",
            "pairMarketcapUsd": "820365.807483577928256",
            "pairMarketcapUsdInitial": "0.21837969976141599998890451689304015303605410736054182052612304687500",
            "pairPrice0Usd": "230.939232",
            "pairPrice1Usd": "26.98523054",
            "pairReserves0": "1776150808979",
            "pairReserves0Usd": "410182.903741788964128",
            "pairReserves1": "76791121807",
            "pairReserves1Usd": "410182.903741788964128",
            "pairTotalSupply": "0",
            "renounced": false,
            "routerAddress": "CAMMCzo5YL8w4VFF8KVHrK22GGUsp5VTaW7grrKgrWqK",
            "routerType": "RAYDIUM_CLMM",
            "token0Address": "So11111111111111111111111111111111111111112",
            "token0Decimals": 9,
            "token0Symbol": "WSOL",
            "token1Address": "6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN",
            "token1BuyFee": 0.0,
            "token1Decimals": 6,
            "token1ImageUri": "https://arweave.net/VQrPjACwnQRmxdKBTqNwPiyo65x7LAT773t8Kd7YBzw",
            "token1IsHoneypot": false,
            "token1IsProxy": false,
            "token1Name": "OFFICIAL TRUMP",
            "token1SellFee": 0.0,
            "token1Symbol": "TRUMP",
            "token1TotalSupply": "999999673025758",
            "token1TotalSupplyFormatted": "999999673.025758",
            "token1TransferFee": 0.0
        },
        "pairStats": {
            "fiveMin": {
                "buyers": 0,
                "buys": 0,
                "buyVolume": "0",
                "change": "0",
                "diff": "0",
                "first": "0",
                "last": "0",
                "makers": 0,
                "sellers": 0,
                "sells": 0,
                "sellVolume": "0",
                "txns": 0,
                "volume": "0"
            },
            "oneHour": {
                "buyers": 1,
                "buys": 1,
                "buyVolume": "41.89998539733300",
                "change": "-1.17998668",
                "diff": "-4.18951741356390646718399425857508085641528029372677424711869486515538402085861846585822283958227537500",
                "first": "28.16521722",
                "last": "26.98523054",
                "makers": 2,
                "sellers": 1,
                "sells": 1,
                "sellVolume": "0.26629025496872",
                "txns": 2,
                "volume": "42.16627565230172"
            },
            "sixHour": {
                "buyers": 5,
                "buys": 11,
                "buyVolume": "2460.44526252880062000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
                "change": "0.83078833",
                "diff": "3.17647122171220641757284106117436484224681157901092167853194679161158069293040373350787663385614982300",
                "first": "26.15444221",
                "last": "26.98523054",
                "makers": 9,
                "sellers": 4,
                "sells": 4,
                "sellVolume": "17.94046817878388000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
                "txns": 15,
                "volume": "2478.38573070758450000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000"
            },
            "twentyFourHour": {
                "buyers": 8,
                "buys": 19,
                "buyVolume": "4060.76041288114673000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
                "change": "-2.71552499",
                "diff": "-9.14294919958219662164937526085889438651596483478412038900749135252721970066328477671557737642507709000",
                "first": "29.70075553",
                "last": "26.98523054",
                "makers": 20,
                "sellers": 17,
                "sells": 75,
                "sellVolume": "24500.448614236881870000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
                "txns": 94,
                "volume": "28561.209027118028600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000"
            }
        }
    },
    "event": "pair-stats"
}
```
<br></br>

# Subscribe to new tokens with filtering
### Request json
```
{
    "data": {
        "a": "",
        "algos": [],
        "callers": [],
        "freezeAuthDisabled": "true",
        "isLPLocked": "true",
        "isNotHP": "true",
        "maxAge": "1",
        "minChg1H": "50",
        "minLiq": "140000",
        "mintAuthDisabled": "true",
        "rankBy": "age",
        "tgConn": []
    },
    "event": "scanner-filter"
}
```
### Response json
```
{
    "data": {
        "filter": {
            "algos": [
            ],
            "callers": [
            ],
            "freezeAuthDisabled": "true",
            "isLPLocked": "true",
            "isNotHP": "true",
            "maxAge": "1",
            "minChg1H": "50",
            "minLiq": "140000",
            "mintAuthDisabled": "true",
            "orderBy": "desc",
            "rankBy": "age",
            "tgConn": [
            ],
            "timeFrame": "24H"
        },
        "results": {
            "pairs": [
                {
                    "age": "2025-01-29T03:50:14Z",
                    "buyFee": 0.0,
                    "buys": 2695,
                    "callCount": 0,
                    "chainId": 900,
                    "contractRenounced": false,
                    "contractVerified": false,
                    "currentMcap": "9358399843.00",
                    "diff1H": "73.15",
                    "diff24H": "73.15",
                    "diff5M": "6.37",
                    "diff6H": "73.15",
                    "discordLink": null,
                    "fdv": "9358399843.00",
                    "first1H": "0.0540475387700000000000000000000000000000",
                    "first24H": "0.0540475387700000000000000000000000000000",
                    "first5M": "0.0879741940900000000000000000000000000000",
                    "first6H": "0.0540475387700000000000000000000000000000",
                    "honeyPot": false,
                    "initialMcap": "5404753877.00",
                    "isFreezeAuthDisabled": true,
                    "isMintAuthDisabled": true,
                    "liquidity": "932683.85",
                    "liquidityLocked": true,
                    "liquidityLockedAmount": null,
                    "liquidityLockedRatio": "1",
                    "makers": 1560,
                    "migratedFromPairAddress": null,
                    "migratedFromRouterAddress": null,
                    "migrationProgress": null,
                    "pairAddress": "GKxYpXbdNzakpwe8Zr2dRUMTnCZsG9wTEKqpsNP3d6BC",
                    "pairMcapUsd": "932683.85",
                    "pairMcapUsdInitial": "708181.67465264728002694027964025735855102539062500",
                    "percentChangeInLiquidity": "31.70",
                    "percentChangeInMcap": "73.15",
                    "price": "0.0935839984300000000000000000000000000000",
                    "reserves0": "2017093979555",
                    "reserves0Usd": "466341.92",
                    "reserves1": "4995514582641",
                    "reserves1Usd": "466341.92",
                    "routerAddress": "675kPX9MHTjS2zt1qfr1NYHuzeLXfQM9H24wFSUt1Mp8",
                    "sellFee": 0.0,
                    "sells": 671,
                    "telegramLink": null,
                    "token0Decimals": 9,
                    "token0Symbol": "WSOL",
                    "token1Address": "Bt6TAHp5JHiwF4aygUxJ28XgMh4Z3NHY13KzShQeqiZJ",
                    "token1Decimals": 6,
                    "token1ImageUri": null,
                    "token1Name": "DeepSeek AI Agent",
                    "token1Symbol": "DeepSeekA",
                    "token1TotalSupplyFormatted": "100000000000",
                    "twitterLink": "https://x.com/donna_mart5387",
                    "txns": 3366,
                    "volume": "1162438.27",
                    "webLink": null
                },
                {
                    "age": "2025-01-29T03:49:39Z",
                    "buyFee": 0.0,
                    "buys": 1533,
                    "callCount": 0,
                    "chainId": 900,
                    "contractRenounced": false,
                    "contractVerified": false,
                    "currentMcap": "4445592846.00",
                    "diff1H": "96.56",
                    "diff24H": "96.56",
                    "diff5M": "6.20",
                    "diff6H": "96.56",
                    "discordLink": null,
                    "fdv": "4445592846.00",
                    "first1H": "0.0002255711577000000000000000000000000000",
                    "first24H": "0.0002255711577000000000000000000000000000",
                    "first5M": "0.0004175016092000000000000000000000000000",
                    "first6H": "0.0002255711577000000000000000000000000000",
                    "honeyPot": false,
                    "initialMcap": "2255711577.00",
                    "isFreezeAuthDisabled": true,
                    "isMintAuthDisabled": true,
                    "liquidity": "704541.93",
                    "liquidityLocked": true,
                    "liquidityLockedAmount": null,
                    "liquidityLockedRatio": "1",
                    "makers": 1023,
                    "migratedFromPairAddress": null,
                    "migratedFromRouterAddress": null,
                    "migrationProgress": null,
                    "pairAddress": "Gb1czU3jsA4vQToW4bJnUT1HAqJpe47wHqmtHNuA44L8",
                    "pairMcapUsd": "704541.93",
                    "pairMcapUsdInitial": "501749.440729978920018083954346366226673126220703125000",
                    "percentChangeInLiquidity": "40.41",
                    "percentChangeInMcap": "97.08",
                    "price": "0.0004445592846000000000000000000000000000",
                    "reserves0": "1523696684620",
                    "reserves0Usd": "352270.96",
                    "reserves1": "794390190780909",
                    "reserves1Usd": "352270.96",
                    "routerAddress": "675kPX9MHTjS2zt1qfr1NYHuzeLXfQM9H24wFSUt1Mp8",
                    "sellFee": 0.0,
                    "sells": 397,
                    "telegramLink": null,
                    "token0Decimals": 9,
                    "token0Symbol": "WSOL",
                    "token1Address": "AeeTkxSwmtLwevfvmB239qFe5PMqtCcPJ9xxkutUrHtH",
                    "token1Decimals": 6,
                    "token1ImageUri": null,
                    "token1Name": "Eric Trump",
                    "token1Symbol": "Eric",
                    "token1TotalSupplyFormatted": "10000000000000",
                    "twitterLink": "https://x.com/erictrump_meme",
                    "txns": 1930,
                    "volume": "664739.50",
                    "webLink": null
                }
            ],
            "stats": {
                "txns": 5296,
                "volume": "1827177.7863688413310190685"
            },
            "totalRows": 2
        }
    },
    "event": "scanner-pairs"
}
```
