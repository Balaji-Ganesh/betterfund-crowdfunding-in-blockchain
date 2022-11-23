## on 22nd Nov, 2022

- Tried to understand the flow of index.js

### doubts

Q: How the home page is loading the active campaigns?

- `getServerSideProps` - Next.js handles it
  - `getServerSideProps` returns JSON which will be used to render the page. All this work will be handled automatically by Next.js, so you don't need to do anything ...
- via .. `factory.methods.getDeployedCampaigns().call();`
  from `/pages/index.js - getServerSideProps()`
- `Campaigns.sol` (Smart contract) - had a method named `getDeployedCampaigns()` - which contains the addresses of all the deployed campaigns.

## On 23rd Nov, 2022

- In understanding the flow..

### doubts..

1. **How page navigation is taking place??**

   - got doubt @ .. How does navigation to specific campaign page taking place when clicked any one of the campaign in home page
   - not used `react-router-dom` .. then how navigation is taking place..??
   - any other way

2. How methods of details are being fetched from deployed campaign

   - `campaign.methods.<method_name>()`
   - from ref of `import Campaign from "../../smart-contract/campaign";`

3. How party-like wrappers _(technically called as **confetti**)_ are made when contribution takes place..??
   - with [react-confetti](https://www.npmjs.com/package/react-confetti)

### new methods of handling / designing

- using `useForm` of `react-hook-form` to handle formdata
  - Checkout [website](https://react-hook-form.com/) -- had option to generate forms online and get react code

## Questions for next day..

1. What is the functionality of `web3.eth.getAccounts();` -- seen at `/pages/campaign/[id].js`
2. What is the meaning of `payable` --- seen at `Campaign.sol` at `contribute()`
