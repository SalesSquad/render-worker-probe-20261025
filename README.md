# Encrypted hosted render worker

Public GitHub-hosted runner shell with encrypted inputs and outputs. No Lieri
source, reference image, rendered frame, or decryption key is public. The
workflow is manually dispatched, decrypts only inside an ephemeral Ubuntu
runner, and uploads only an AES-256-encrypted result.

The symmetric key is retained only in the local ignored file
`.lieri-payload-key` with owner-only permissions so completed artifacts can be
decrypted after download.
