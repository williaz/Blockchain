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
