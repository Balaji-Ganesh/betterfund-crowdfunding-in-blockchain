## on 22nd Nov, 2022

- Tried to understand the flow of index.js

### doubts

Q: How the home page is loading the active campaigns?

- `getServerSideProps` - Next.js handles it
  - `getServerSideProps` returns JSON which will be used to render the page. All this work will be handled automatically by Next.js, so you don't need to do anything ...
- via .. `factory.methods.getDeployedCampaigns().call();`
  from `/pages/index.js - getServerSideProps()`
- `Campaigns.sol` (Smart contract) - had a method named `getDeployedCampaigns()` - which contains the addresses of all the deployed campaigns.
