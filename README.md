# The Web3 Index

The Web3 Index tracks key usage metrics for protocols across the entire Web3 stack so you can stay up to date on the latest Web3 trends whether you’re a supply-side participant / investor keeping tabs on in-demand networks, a developer interested in building on top of the most promising Web3 infrastructure, or simply a crypto-enthusiast passionate about the Web3 movement.

Unlike most indexes in the Web3 space that use market capitalization or ["total locked value (TLV)"](https://messari.io/article/how-to-interpret-total-value-locked-tvl-in-defi), The Web3 Index uses a [fundamental index methodology](https://en.wikipedia.org/wiki/Fundamentally_based_indexes). A key belief behind the fundamental index methodology is that underlying valuation figures (i.e. network revenue and usage) are more accurate estimators of a network's intrinsic value, rather than the listed market value of the project. In the spirit of this methodology, you won't see any token prices on The Web3 Index.

## Submiting a Project

1. Go to the "Issues" tab above
2. Click "New Issue"
3. Select "Project Submission"
4. Fill in the template
5. Submit

## How to Provide Revenue Data For Project Submission

In order for a project to be considered for the index, its revenue data must be surfaced in a format that's consumable by the application. If the project you'd like to add to the index is built on Ethereum or any other blockchain supported by The Graph, we recommend adding it The Web3 Index subgraph. You can find instructions on how to add a project to the subgraph [here](https://github.com/web3index/subgraph).

If a project's blockchain is not supported by The Graph, you'll have to provide this data via a publically accessible endpoint with a json response that adheres to the following schema:

```
{
  "revenue": {
    "now": 61779.07, // total revenue as of now
    "oneDayAgo": 60579.17, // total revenue as of 1 day ago
    "twoDaysAgo": 60390.5, // total revenue as of two days ago
    "oneWeekAgo": 58620.2, // total revenue as of one week ago
    "twoWeeksAgo": 53635.26 // total revenue as of two weeks ago
  },
  "days": [
    {
      "date": 1578960000, // timestamp representing start of day at 12:00 am UTC
      "revenue": 843.22 // total revenue as during this day
    }
    //...
  ]
}
```

Once you've successfully provided this information the project can be added to the [registry file](./registry.json).

## Running App Locally

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
