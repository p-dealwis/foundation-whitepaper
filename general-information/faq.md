# FAQ

## What is a user binding authentication?

A binding authentication ties the user to something else they have access to such as a mobile phone or an email address. This way user doesn't have to memorise passwords and will allow more seamless flows when [Wallet Retrieval](../technology/wallet-retrieval.md) happens.

## Why are regular key rotations of a service's keys necessary?

 Key rotations are important since bad actors may have acquired the service's keys without the service's express knowledge. Typically bad actors will acquire keys of different services over time and arrange an attack on the vault which is now essentially a honey pot. A regular key rotation will mean hackers will have to attack  the service and the vault at the same time which would be very hard to coordinate.

Regular key rotations are also an industry best practise and the vault should faciliate these rotations by providing simple functions the service can use on a regular basis. These functions should be free to use to encourage key rotations.



