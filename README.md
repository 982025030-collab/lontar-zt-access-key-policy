# Metadata patch v1.3.1

Corrects inherited `.zenodo.json` version/description from v1.3.0. The timing supplement and all measured data remain byte-identical. v1.3.0 Zenodo record 23804695 contains the correct v1.3.0 archive but inherited v1.2.0 descriptive metadata; use the v1.3.1 record [10.5281/zenodo.23804786](https://doi.org/10.5281/zenodo.23804786).

# LONTAR-ZT access-key research artifact v1.3.0

Adds a separate timing/instrumentation and server policy-lock amendment with 135 HTTP responses and 54 issue/use timing pairs on 29 October 2026. All 122 instrumented evidence queries retain numerical durations, including failed paths. Nine server-lock probes deny overrides before handler key attempt. Actual planned-versus-observed delays, cold-start outliers and all failures remain in the results. Reanalysis of all 180 v1.2.0 issue/use pairs corrects the interpretation of planned 50-ms profiles; the original measurements and archive remain unchanged.

New supplement: `LONTAR_AKP_Timing_Amendment_v1.3.0.zip`. Clean-extraction standard-library reanalysis, 23 offline tests (boto3 with mocked AWS calls), and input-tamper rejection pass. All three Lambda code/environment configurations and state were restored; host stopped. One host-day supplies descriptive staging evidence only. The 28 handler-recorded KMS successes have no new CloudTrail capture and are not added to the earlier 191 correlated operations. The formatted article/report are not included.

Metadata patch v1.3.1: [Zenodo DOI 10.5281/zenodo.23804786](https://doi.org/10.5281/zenodo.23804786). DOI 10.5281/zenodo.23734013 identifies the unchanged historical v1.2.0 snapshot, not this amendment. No primary test, old archive, or old release/tag is replaced.

# LONTAR-ZT access-key research artifact v1.2.0

Adds the separate `LONTAR_AKP_AWS_Robustness_Supplement_v1.2.0.zip`. The primary v1.0.0 ZIP and earlier v1.1.1 supplement remain byte-identical. This is a new execution campaign, not a changed primary test.

The new supplement retains 539 HTTP responses and 180 boundary-use trials from project 501250588559/ap-southeast-2. All 191 successful KMS operations correlate with CloudTrail. One unexpected recovery 503 remains in the dataset. An actual unpublished guest posture change was still authorized using a 14.596-second-old signed observation: this is a source-freshness counterexample, not a claimed protection. See the supplement README for reanalysis, matched overhead, fail-closed behavior, fault mechanisms and limitations.

Public clean-extraction numerical reanalysis passes; all 12 offline contract tests pass; tampered data are rejected. Retrospective comparison against the byte-identical primary archive verifies 53 protected files and finds equal outcomes for exact screening, empirical screening and fixed P60. Neither requests nor four sequential benchmark blocks establish independent host-days. No risk certificate is transferred to AWS. No hardware-attested, independent-site, settled-cost or production claim is made.

Version-specific archive: [Zenodo DOI 10.5281/zenodo.23734013](https://doi.org/10.5281/zenodo.23734013). The downloaded Zenodo archive contains a byte-identical v1.2.0 supplement and original primary ZIP. The historical DOI below identifies v1.1.1 only. The formatted revised manuscript is not part of this public artifact.

# Earlier artifact v1.1.1 (retained unchanged)

Research artifact by Meiton Boru, Irwan Sembiring, and Wiwin Sulistyo, Faculty of Information Technology, Satya Wacana Christian University, Salatiga, Indonesia.

This artifact accompanies *Evidence-Aware Risk-Bounded Access--Key Policy Selection for Zero-Trust Data Centers*. It implements a constrained selector over six complete access--key policies: permit lifetime (2 or 60 seconds), and either offline enforcement or online evidence revalidation with 0.1- or 0.5-second deadlines. It uses disjoint tuning (16 blocks), certification (107 blocks), and untouched test (100 blocks) splits. Together these contain 9,366 measured requests.

Version 1.1.1 immutable archive: [Zenodo DOI 10.5281/zenodo.23724800](https://doi.org/10.5281/zenodo.23724800).

Version 1.1.1 fixes public reanalysis: the analyzer verifies PUBLIC_SHA256.json when the intentionally excluded private per-run manifest is unavailable. Clean extraction reproduces all outcomes, all 12 offline contract tests pass, and a modified measurement file is rejected. Measurements and AWS runtime code are unchanged. Version 1.1.0 remains at [its historical DOI](https://doi.org/10.5281/zenodo.23723261); use the patch for executable public reanalysis.

## Version 1.1.1 AWS supplement

The original `LONTAR_ZT_Access_Key_Research_Artifact_v1.0.0.zip` remains byte-identical. Its article source is historical. The new `LONTAR_AKP_AWS_Contract_Supplement_v1.1.1.zip` adds reviewed cloud source, selected byte-identical outcome/audit files, provenance, checksums, reanalysis, and the CRediT statement. It does not contain the revised manuscript PDF or claim to archive every historical October artifact.

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
