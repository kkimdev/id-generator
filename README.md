# ID Generator
Desired properties:
- Can contain fixed or variable length binary data
- Tiered permissions
  - Cannot do anything
  - Can verify integrity and authenticaion
  - Can verify integrity and authenticaion + can read data
  - Can verify integrity and authenticaion + can create id (probably we don't need this tier, but can be achieved with public-key encryption)
  - Can verify integrity and authenticaion + can read data + can create id

# Design notes
1. Optional random paddng TODO: is there a better padding strategy?
2. Apply Feistel cipher with AES or ChaCha20 TODO: consider FF1 nide
3. Append HMAC(SHA) output

# Other ID formats
- UUID https://en.wikipedia.org/wiki/Universally_unique_identifier
- JWT https://en.wikipedia.org/wiki/JSON_Web_Token

# References
- https://en.wikipedia.org/wiki/Probabilistic_encryption
- https://en.wikipedia.org/wiki/Format-preserving_encryption
- https://en.wikipedia.org/wiki/HMAC
- https://en.wikipedia.org/wiki/Feistel_cipher
