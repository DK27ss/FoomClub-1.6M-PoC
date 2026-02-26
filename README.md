# Foom

[https://basescan.org/tx/0xa88317a105155b464118431ce1073d272d8b43e87aba528a24b62075e48d929d](https://app.blocksec.com/phalcon/explorer/tx/base/0xa88317a105155b464118431ce1073d272d8b43e87aba528a24b62075e48d929d)

[https://etherscan.io/tx/0xce20448233f5ea6b6d7209cc40b4dc27b65e07728f2cbbfeb29fc0814e275e48](https://app.blocksec.com/phalcon/explorer/tx/eth/0xce20448233f5ea6b6d7209cc40b4dc27b65e07728f2cbbfeb29fc0814e275e48)

vulnerable : https://basescan.org/address/0x02c30d32a92a3c338bc43b78933d293ded4f68c6

Cryptographic issue in the ZK Verifier

Broken Groth16 Trusted Setup (delta == gamma == G2 generator)
The victim contract is a lottery/gambling contract that uses ZK proofs (Groth16) for withdrawals.
The ZK Verifier contract has a fatal cryptographic flaw - the verification key's delta and gamma parameters are identical - both set to the BN254 G2 generator point

