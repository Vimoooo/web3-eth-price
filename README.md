const axios = require("axios");

async function getETHPrice() {
  try {
    const { data } = await axios.get(
      "https://api.coingecko.com/api/v3/simple/price?ids=ethereum&vs_currencies=usd"
    );

    console.log(`ETH Price: $${data.ethereum.usd}`);
  } catch {
    console.log("Failed to fetch ETH price.");
  }
}

getETHPrice();
