<div align="right">

  [![license](https://img.shields.io/github/license/block-foundation/docker-algorand-indexer?color=green&label=license&style=flat-square)](LICENSE.md)
  ![stars](https://img.shields.io/github/stars/block-foundation/docker-algorand-indexer?color=blue&label=stars&style=flat-square)

</div>

---

<div>
    <img align="right" src="https://raw.githubusercontent.com/block-foundation/brand/master/logo/logo_gray.png" width="96" alt="Block Foundation Logo">
    <h1 align="left">Algorand Indexer</h1>
    <h3 align="left">Block Foundation Docker Containers</h3>
</div>

---

<p align="center">
    <img src="https://raw.githubusercontent.com/block-foundation/docker-algorand-indexer/master/res/block_foundation-containers.jpg"width="100%" height="100%" alt="Form Follows Finance">
</p>

The primary purpose of this Indexer is to provide a REST API interface of API calls to support searching the Algorand Blockchain. The Indexer REST APIs retrieve the blockchain data from a PostgreSQL compatible database that must be populated. This database is populated using the same indexer instance or a separate instance of the indexer which must connect to the algod process of a running Algorand node to read block data. This node must also be an Archival node to make searching the entire blockchain possible.

## Network

``` mermaid
stateDiagram
    Blockchain --> Node
    Node --> Blockchain
    Node --> Indexer
    state Indexer {
      Service --> Database
      Database --> Service
    }
    Indexer --> SDK
    state SDK {
      Python
      JavaScript
      Go
      Java
    }
```

## Resources

### Algorand

- [Algorand](https://www.algorand.com/)
- [Algorand | Developer](https://developer.algorand.org/)

#### Algorand SDK

- [Algorand SDK | Docs](https://py-algorand-sdk.readthedocs.io/en/latest/)
- [Algorand SDK | GitHub](https://github.com/algorand/py-algorand-sdk/)

#### Algorand Go

- [Algorand Go | GitHub](https://github.com/algorand/go-algorand)

#### AlgoDjango
- [AlgoDjango | Tutorial](https://developer.algorand.org/solutions/getting-started-with-python-algorand-sdk-and-django/)
- [AlgoDjango | GitHub](https://github.com/ipaleka/algodjango)

#### Algorand PyTeal

- [Algorand PyTeal](https://github.com/algorand/pyteal)
- [Algorand PyTeal | Utils](https://github.com/algorand/pyteal-utils)
- [Algorand PyTeal | Course](https://github.com/algorand-devrel/pyteal-course)

#### Algorand Sandbox

- [Algorand Sandbox](https://github.com/algorand/sandbox)

## Legal

### Copyright

Copyright &copy; 2023 [Block Foundation](https://www.blockfoundation.io/ "Block Foundation website"). All Rights Reserved.

### License

Except as otherwise noted, the content in this repository is licensed under the
[Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/), and
code samples are licensed under the [MIT License](https://opensource.org/license/mit/).

Also see [LICENSE](https://github.com/block-foundation/community/blob/master/LICENSE) and [LICENSE-CODE](https://github.com/block-foundation/community/blob/master/LICENSE-CODE).

### Disclaimer

**THIS SOFTWARE IS PROVIDED AS IS WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
