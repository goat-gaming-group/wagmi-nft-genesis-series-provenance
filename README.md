# WAGMI NFT Genesis Series Provenance

At WAGMI we believe in transparency, therefore we have decided to use a provenance hash to prove there has been no tampering with the assignment of the NFTs in the genesis series. The provenance hash was set in the contract as a constant at the point of deployment, prior to any NFTs being minted, and cannot be modified in any way.

The provenance hash for WAGMI NFT Genesis Series is:

```bash
f2982d58f8ec0a86a0d69a08778f8c2c1e493296ccabb59ff695c7a01a1c631c
```

You can further validate the hash exists on the `PROVENANCE` field in our [smart contract](https://etherscan.io/address/0xa7d107c55566282dee5c0ff65522d6e6aca748ca#readContract#F2) as well as in the following [file in this repository]().

## What is a provenance?

Provenance refers to the origin of an object. A provenance hash, is a unique digital fingerprint that is associated with an NFT (non-fungible token) drop and is used to verify the authenticity and provenance of an NFT. You can read more about provenance hashes from [this article](https://dev.to/brodan/learning-nft-provenance-by-example-a-bored-ape-investigation-hfe) that uses [BAYC](https://boredapeyachtclub.com/#/) as an example.

## How was it calculated for the NFT Genesis Series

For the hash generation we use SHA-256 cryptographic hash functions. In order to verify authenticity and for you to generate hashes it is imperative that the same hashing algorithm is used.

- First, we generated the hash of each image - which you can find in the respective `hashes/{imageId}.txt` file.
- Secondly, we concatenated all the resulting hashes into a single huge string - which you can see in [this file]().
- Finally, we hashed the contents of the concatenated string, which gave us the _provenance_ hash used in the smart contract.
