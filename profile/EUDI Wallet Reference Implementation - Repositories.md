# EUDI Wallet Reference Implementation - Repositories

The EUDI Wallet Reference Implementation is based on a modular architecture composed of a set of business agnostic, re-usable components which will be evolved in incremental steps and can be re-used across multiple projects. This document provides an overview of the key repositories of the EUDI Reference Implementation. 

Specifically, as part of the EUDI Wallet Reference Implementation, the following set of components are being delivered:

- 📚[Libraries and other software components needed to the framework](#libraries)
- 🛡️[Verifier mobile native applications and services for proximity and remote flows](#verifier-apps-and-services)
- 📝[Issuer applications and services](#issuing-apps-and-services)
- 📱[EUDI Wallet mobile native applications for issuing, proximity and remote flows](#eudi-wallet-mobile-native-applications)
- ✍️[Remote electronic signing applications and services](#signing-apps-and-services)


## Libraries

### Wallet Core (Android) and Wallet Kit (iOS) Coordinator Libraries

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [Wallet Core (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-android-wallet-core) | Implementation of the EUDI Wallet Core library for Android that serves as a coordinator layer between the UI app and the Wallet libraries. Currently, coordinates issuing, proximity and remote presentation libraries. |
| [Wallet Kit (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-wallet-kit) | Implementation of the EUDI Wallet Kit library for iOS that serves as a coordinator layer between the UI app and the Wallet libraries. Currently coordinates issuing, proximity and remote presentation libraries.      |

### Proximity Sharing iOS Libraries

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [mDoc Security (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-iso18013-security)      | Implementation of mDoc security mechanisms according to ISO/IEC 18013-5.|
| [mDoc Data Transfer (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-iso18013-data-transfer) | Implementation of the mDoc data-transfer library according to ISO/IEC 18013-5.| 
| [mDoc Data Model (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-iso18013-data-model)    | Implementation of the mDoc data-model according to ISO/IEC 18013-5.| 


### Proximity Sharing Android Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [mDoc Data Transfer (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-android-iso18013-data-transfer) | This library provides a set of classes to manage the transfer of documents in an EUDI ISO 18013-5 Android Wallet. |

### Remote Presentation iOS Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Presentation Exchange (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-presentation-exchange-swift)        | Implementation of DIF Presentation Exchange v2 specification in Swift.     | 
| [SIOPv2 & OpenID4VP protocols (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-siop-openid4vp-swift) | Implementation of SIOPv2 and OpenID4VP (draft 24) protocols (wallet's role) in Swift. |
| [SD-JWT (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-sdjwt-swift)                       | SD-JWT library for creating and verifying SD-JWT in JVM Swift.             | 


### Remote Presentation Android Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Presentation Exchange (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-presentation-exchange-kt)        | Implementation of DIF Presentation Exchange v2 specification in Kotlin.     |
| [SIOPv2 & OpenID4VP protocols (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-siop-openid4vp-kt) | Implementation of SIOPv2 and OpenID4VP (draft 24) protocols (wallet's role) in Kotlin. | 
| [SD-JWT (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-sdjwt-kt)                        | SD-JWT library for creating and verifying SD-JWT in JVM Kotlin.             | 

### Ιssuing iOS Libraries

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [OpenId4VCI (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-openid4vci-swift) | Implementation of credential management supporting the OpenId4VCI (draft 15) protocol. | 

### Ιssuing Android Libraries

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [OpenId4VCI (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-openid4vci-kt)      | Implementation of credential management supporting the OpenId4VCI (draft 15) protocol.|

### Wallet Data Storage and Cryptographic Management iOS Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [mDoc Document Storage (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-wallet-storage) |  Storage for keys and wallet documents |

### Wallet Data Storage and Cryptographic Management Android Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [mDoc Document Storage (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-android-wallet-document-manager)    | This library provides a set of classes to manage documents and their cryptographic keys in an EUDI Android Wallet. |


### Revocation Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Token Status List (Kotlin)](https://github.com/eu-digital-identity-wallet/eudi-lib-kmp-statium) |  Statium is a Kotlin multiplatform library supporting JVM and Android platforms. It implements the Token Status List Specification draft 10, and allows callers to check the status of a "Referenced Token" as defined in the specification, effectively enabling applications to verify if tokens are valid, revoked, or in other states. |
| [Token Status List (Swift)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-statium-swift) |  Statium is a Swift library for iOS and macOS. It implements the Token Status List Specification draft 10, and allows callers to check the status of a "Referenced Token" as defined in the specification, effectively enabling applications to verify if tokens are valid, revoked, or in other states.|


### rQES: Low Level Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [EUDI rQES CSC library (Kotlin)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-rqes-csc-kt) |  This is a Kotlin library targeting JVM, that supports the Cloud Signature Consortium API (version 2) protocol. |
| [EUDI rQES CSC library (Swift)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-rqes-csc-swift) |  This is a Swift library targeting JVM, that supports the Cloud Signature Consortium API (version 2) protocol. |

### rQES: Core and Kit Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [EUDI Remote Qualified Electronic Signature (RQES) Core library for Android](https://github.com/eu-digital-identity-wallet/eudi-lib-android-rqes-core) |  This module provides the core functionality for the EUDI Wallet for Android, focusing on the Remote Qualified Electronic Signature (RQES) service. |
| [EUDI Remote Qualified Electronic Signature (RQES) Core library for iOS](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-rqes-kit) |  This module provides the core functionality for the EUDI Wallet for iOS, focusing on the Remote Qualified Electronic Signature (RQES) service. |

### rQES: UI Libraries

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [EUDI Remote Qualified Electronic Signature (RQES) UI library for Android](https://github.com/eu-digital-identity-wallet/eudi-lib-android-rqes-ui) |  TThis module provides the core and UI functionality for the EUDI Wallet for Android implementation, focusing on the Remote Qualified Electronic Signature (RQES) service.|
| [EUDI Remote Qualified Electronic Signature (RQES) UI library for iOS](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-rqes-ui) |  This package provides the core and UI functionality for the EUDI Wallet for iOS implementation, focusing on the Remote Qualified Electronic Signature (RQES) service.|


</br>

## EUDI Wallet mobile native applications

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Wallet UI App (Android)](https://github.com/eu-digital-identity-wallet/eudi-app-android-wallet-ui) | Implementation of wallet UI app for Android. Currently, it also includes Demo App, demonstrating the following capabilities: Proximity presentation, Same Device Online Authentication and issuing of PID and mDL.	 |
| [Wallet UI App (iOS)](https://github.com/eu-digital-identity-wallet/eudi-app-ios-wallet-ui) | Implementation of wallet UI app for iOS. Currently, it also includes Demo App, demonstrating the following capabilities: Proximity presentation, and Same Device Online Presentation and issuing of PID and mDL.| 

</br>

## Verifier Apps and Services

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Web Verifier](https://github.com/eu-digital-identity-wallet/eudi-web-verifier)               | Demo Web Verifier UI application (Frontend) that acts as a Verifier/RP trusted end-point. Available at [https://verifier.eudiw.dev](https://verifier.eudiw.dev)  |  
| [Restful API (web-services)](https://github.com/eu-digital-identity-wallet/eudi-srv-web-verifier-endpoint-23220-4-kt)             | Demo Web Verifier application (Backend Restful service) that acts as a Verifier/RP trusted end-point.| 

</br>

## Issuing Apps and Services

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [OpenId4VCI issuer (Python)](https://github.com/eu-digital-identity-wallet/eudi-srv-web-issuing-eudiw-py)               | An implementation of a credential issuing service, according to OpenId4VCI (draft 15), in Python. Available at https://issuer.eudiw.dev/  |  
| [OpenId4VCI issuer (Kotlin)](https://github.com/eu-digital-identity-wallet/eudi-srv-pid-issuer)             | An implementation of a credential issuing service, according to OpenId4VCI (draft 15), in JVM Kotlin. Available at  https://issuer-backend.eudiw.dev/ | 


</br>

## Signing Apps and Services

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Trust Provider Signer](https://github.com/eu-digital-identity-wallet/eudi-srv-web-trustprovider-signer-java)               | TrustProvider Signer is a remote signing service provider and client. The trustprovider signer can be accessed using the EUDI Wallet through OID4VP presentation of the PID. Available [here](https://trustprovider.signer.eudiw.dev/tester)  |  
| [EUDI Wallet-driven signer QTSP](https://github.com/eu-digital-identity-wallet/eudi-srv-web-walletdriven-rpcentric-signer-qtsp-java)               | Implementation of a wallet-driven QTSP for the remote Qualified Electronic Signature component of the EUDI Wallet. The QTSP provides endpoints based on the CSC API v2.0 specification and supports authentication via OpenID4VP.|  
| [EUDI Wallet-driven external SCA](https://github.com/eu-digital-identity-wallet/eudi-srv-web-walletdriven-signer-external-sca-java)               | Implementation of a wallet-driven SCA for the remote Qualified Electronic Signature component of the EUDI Wallet. The SCA provides endpoints that allow to calculate the hash value of a document and obtain the signed document given the signature value.|  
| [RP Centric rQES SCA](https://github.com/eu-digital-identity-wallet/eudi-srv-web-rpcentric-signer-sca-java)               | This is a REST API server implementing the RP-centric SCA for the remote Qualified Electronic Signature (rQES) component of the EUDI Wallet.|  
