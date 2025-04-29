# Decentralized Identity Management Contract

A secure, decentralized identity management system built on blockchain technology that allows users to register and manage their digital identities without relying on centralized authentication providers.

## Features

- **Identity Registration**: Users can create a self-sovereign digital identity with handle and contact information
- **Profile Management**: Update identity information and avatar images
- **Privacy Control**: Users maintain ownership and control of their identity data
- **Blockchain Security**: Leverages blockchain immutability and cryptographic security
- **Decentralized Architecture**: No central authority or single point of failure

## Contract Functions

### Public Functions

- `register-identity`: Create a new identity with a handle and contact information
- `update-identity`: Update an existing identity's handle and contact details
- `set-avatar`: Set or update the avatar image URL for an identity
- `get-identity-info`: Retrieve information about a specific identity
- `get-identity-count`: Get the total number of registered identities
- `is-identity-registered`: Check if a specific principal has registered an identity

### Input Validation

The contract includes built-in validation to ensure:
- Handles are between 3-50 characters
- Contact information is properly formatted (5-100 characters, contains '@' and '.')
- Avatar URLs meet required format standards

## Usage Examples

### Registering a New Identity

```clarity
(contract-call? .decentralized-identity register-identity "satoshi" "satoshi@blockchain.org")
```

### Updating Identity Information

```clarity
(contract-call? .decentralized-identity update-identity "satoshi_nakamoto" "satoshi@bitcoin.org")
```

### Setting an Avatar Image

```clarity
(contract-call? .decentralized-identity set-avatar "https://example.com/avatars/satoshi.png")
```

### Retrieving Identity Information

```clarity
(contract-call? .decentralized-identity get-identity-info 'ST1PQHQKV0RJXZFY1DGX8MNSNYVE3VGZJSRTPGZGM)
```
