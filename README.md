# LONTAR-ZT access--key policy selection: research artifact v1.0.0

Research artifact by Meiton Boru, Irwan Sembiring, and Wiwin Sulistyo, Faculty of Information Technology, Satya Wacana Christian University, Salatiga, Indonesia.

This artifact accompanies *Evidence-Aware Risk-Bounded Access--Key Policy Selection for Zero-Trust Data Centers*. It implements a constrained selector over six complete access--key policies: permit lifetime (2 or 60 seconds), and either offline enforcement or online evidence revalidation with 0.1- or 0.5-second deadlines. It uses disjoint tuning (16 blocks), certification (107 blocks), and untouched test (100 blocks) splits. Together these contain 9,366 measured requests.

## Contents

- `access_key_testbed/v4/`: frozen protocol, service implementation, selector, runner, tests, source analyses, and complete result logs.
- `access_key_testbed/v3/run_pilot.py`: PKI helper imported by the v4 laboratory runner.
- `access_key_testbed/v2/`: dependency provenance needed to stage the identity-provider runtime.
- `article_source/`: editable article source, bibliography, figure source, and submission-status documentation.

Run `python3 access_key_testbed/v4/test_selector.py` for selector checks. Read `access_key_testbed/v4/README.md` and `ANALYSIS_PLAN.md` before reproducing any campaign. The main experiment requires a local Keycloak/Java staging environment documented in the v2 provenance; vendor binaries are intentionally excluded.

## Scope and limitations

The reported confidence limits use blocks, not individual requests, and are conditional on the frozen laboratory generator. Services are process-separated but run on one physical host. The artifact does not establish independence or generalization across hosts, devices, days, administrators, or sites. The posture signal is a local file-permission mode plus a controlled entitlement record; it is not remote attestation, TPM/TEE verification, secure boot, EDR, or comprehensive endpoint health. Resource-entitlement revocation is not IdP logout or distributed token revocation.

No production credentials, runtime private keys, bearer tokens, object keys, vendor binaries, external traffic datasets, downloaded papers, or formatted manuscript PDF are included. Search and audit the package again before each release.

## License and citation

Original Python source is MIT-licensed; synthetic measurements and original documentation are CC BY 4.0. See `LICENSE` and `LICENSE-DATA.md`. Cite the tagged GitHub release and linked Zenodo record after DOI minting.
