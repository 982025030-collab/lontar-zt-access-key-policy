# LONTAR-ZT access--key policy selection: research artifact v1.1.0

Research artifact by Meiton Boru, Irwan Sembiring, and Wiwin Sulistyo, Faculty of Information Technology, Satya Wacana Christian University, Salatiga, Indonesia.

This artifact accompanies *Evidence-Aware Risk-Bounded Access--Key Policy Selection for Zero-Trust Data Centers*. It implements a constrained selector over six complete access--key policies: permit lifetime (2 or 60 seconds), and either offline enforcement or online evidence revalidation with 0.1- or 0.5-second deadlines. It uses disjoint tuning (16 blocks), certification (107 blocks), and untouched test (100 blocks) splits. Together these contain 9,366 measured requests.

## Version 1.1.0 AWS supplement

The original `LONTAR_ZT_Access_Key_Research_Artifact_v1.0.0.zip` remains byte-identical. Its article source is historical. The new `LONTAR_AKP_AWS_Contract_Supplement_v1.1.0.zip` adds reviewed cloud source, selected byte-identical outcome/audit files, provenance, checksums, reanalysis, and the CRediT statement. It does not contain the revised manuscript PDF or claim to archive every historical October artifact.

The earlier 22/27 October implementation retains 235 observations, including failed recovery, delayed KMS-denial behavior and HTTP 429 responses. A separate 28 October run uses three Lambda roles, KMS-signed bound permits with maximum 60-second lifetime, nonce-bound use-time evidence with a 500-ms retrieval deadline, atomic replay consumption, and a post-query expiry check. Its 52 route observations comprise 25 permit issues, 12 successful key operations, and 15 negative cases matching expected statuses. The host was verified stopped and collector configuration restored. The supplement report explains each gate and limitations.

This is functional contract alignment with local P60, not identical cryptographic endpoints or certificate transfer. AWS uses ECDSA/GenerateDataKey, Cognito machine identities, and signed SSM operational telemetry. It does not demonstrate human PKCE negative cases, hardware attestation, independent-site generalization, settled monetary cost, or production governance. The 28 October negative-operation claims are handler evidence; no new CloudTrail capture was included.

To reanalyse, extract the supplement and run `python3 analyze_p60.py`. To run the 12 offline contract checks: `python3 -m unittest discover -s aws_isolated -p test_p60_contract.py -v`. Cloud deployment is a separate, billable operation requiring an authorized project, fresh STS verification, and a private resource journal; do not treat offline tests as cloud execution.

The new supplement provides `PUBLIC_SHA256.json` for its distributed bytes. Private per-run manifests reference excluded journals and telemetry, so they are not substituted for the public manifest. The old primary experiment remains separate from all AWS observations; requests do not replace independent host-day groups.

## Original artifact contents

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
