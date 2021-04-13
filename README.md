# Blockchain

- Hash
  - Collision free: nobody can find
    - as message digest: small, validate
  - Hiding: input
    - commitment
      - com, key := commit(msg) := (H(key | msg), key)
      - match := verify(com, key, msg)
  - puzzle-friendly: just try random value
    - mining
  - SHA-256

- Hash pointer
  - H(hp) = data
  - build data structute with hash pointer
  - tamper-evident log
  - Merkle tree: binary tree with hp
    - remember root hash, verify data in O(logN)
    - sorted: O(logN) non-member

- Digital Signature
  - only you can sign, anyone can verify
  - tie to doc
  - (sk, pk) := genKey
  - sig := sign(sk, msg)
  - isValid := verify(pk, msg, sig)
  - sign a hash pointer
  - Bitcoin: ECDSA, good randomness
