# Contributing to BitNet

Contributions improve this fork's BitNet inference implementation, build support, examples, and reproducible performance evidence. Preserve upstream attribution and explain whether a change is fork-specific or suitable for upstream.

## Before you start

Read the [README](README.md), [build configuration](CMakeLists.txt), and applicable platform setup instructions. Identify the CPU/GPU path, quantization format, and model layout affected by the proposed change.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

Use the README's environment and model setup for the selected platform, with dependencies declared in [requirements.txt](requirements.txt). Avoid assuming that a command tested on one compiler, processor, or model format works on another.

For correctness changes, provide a small reproducible case and compare the affected outputs with an appropriate reference. For benchmark changes, record hardware, compiler options, thread count, model identity, prompt and generation lengths, warm-up conditions, and repeated measurements. The README documents the benchmark scripts and their arguments; use those interfaces and report the exact command executed.

Keep downloaded weights and generated benchmark artifacts out of unrelated code changes. Document model redistribution terms separately from source-code licensing. A successful build or benchmark run is evidence for that configuration, not proof of general model quality.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `main` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

For vulnerabilities affecting upstream Microsoft code, follow the [repository security policy](SECURITY.md) and its MSRC reporting route. For fork-specific concerns, follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md), using GitHub's private reporting option if available. Request a private contact if needed without disclosing vulnerability details publicly. Keep credentials, personal data, and unredacted logs out of commits and examples.

## Licensing and conduct

Respect the [existing license](LICENSE) and preserve third-party notices. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [repository code of conduct](CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
