# Delegated Access

Typically a services require users to create their own wallets to interact with the blockchain. This can be quite a large barrier to entry for most consumers since it results in quite a cumbersome on-boarding process. To improve this process cloud wallet can be employed but this results in a honey pot of valuable wallet credentials for bad actors to exploit. To greatly reduce the risks of cloud wallets while enabling convenient customer access, delegated access via Foundation should be used.

After user binding authentication is achieved between the vault and the service's user, the vault can create a wallet for a service user in a sandbox environment, encrypt it using the service's public key and finally commit it to storage. From here on the service can request access to a user's wallet stored in the vault \([Wallet Retrieval](../technology/wallet-retrieval.md)\) only through specific consent from the user, which is now enforced by the vault authenticating the user on each delegated access request from the service. The authentication will be made through a direct communication channel between the vault and user. The user will have to present this data to the service so it may access the wallet on the user's behalf.

## Risk mitigation

* Service IP white listing by the vault,  
* wallet never leaves the vault and service bubble,
* service access audit log and access pattern checking,
* spreading out data required to access a wallet between two parties \(the vault and service\),
* the vault is not privy to wallet data and therefore is not a honey pot.

