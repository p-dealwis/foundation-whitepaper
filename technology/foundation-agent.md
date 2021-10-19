---
description: Service side helper agent
---

# Foundation Agent

The Foundation Agent will live on the service's infrastructure and communicate with  the Vault on behalf of the Service. Designed to be a black box for wallet related functionality. The Service's products will be able to communicate with the Foundation Agent through API requests.

## Features

* Wallet retrieval
* Wallet encryption and decryption
* Wallet creation
* Key rotation
* Blockchain transaction signing
* Encryption as a service

### Agent API

The agent will expose a simple API with to facilitate the features above. Every tasks should be an explicit request to the Foundation Agent, i.e. the key rotation scheduling should be on the Service side.

### Key Store Access

The agent will need to communicate with the Service's secrets store for tasks such as wallet decryption, encryption and key rotation to name a few. Due to the large number of different key stores that can be used by Service's there will be plug-ins developed for the agent to integrate with various key stores such as AWS Secret Manager or Azure Keyvault.

### Vault Authentication

The same authentication procedure that would be used by the Service when directly talking to the the Vault will be employed when the Foundation Agent communicates with the Vault. Furthermore the agent's IP will have to be whitelisted as per the Vault's requirements.
