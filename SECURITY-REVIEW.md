# 🔐 Security Review - assistant-doc-benchmark

## Scope
- Repository contains benchmarking documentation for evaluating AI assistants.
- No application source code, binaries, or infrastructure-as-code are present in the tree, reducing direct attack surface for code-level vulnerabilities.

## Positive Observations
- Project structure is documentation-centric (markdown guides, prompts, evaluation matrices) with no executable assets or configuration files that expose credentials or runtime secrets. This limits the risk of shipping vulnerable code or accidentally deploying unsafe services.
- Credential usage is delegated to official vendor CLIs (`@google/gemini-cli`, `@openai/codex`) with authentication handled through their built-in commands instead of storing tokens in the repository.

## Risks & Findings
1. **Residual Personally Identifiable Information (PII)**
   - The shared benchmark prompt embeds an absolute macOS path that exposes a contributor's username. Publishing such paths can reveal workstation naming conventions or user identities.
2. **Implicit Handling of API Keys**
   - Documentation relies on pre-existing `GEMINI_API_KEY` configuration and interactive authentication commands. While secrets are not stored in-repo, the guides do not remind contributors to avoid committing credentials or shell history containing tokens.
3. **Third-Party CLI Supply Chain Exposure**
   - Test setup requires global installation of vendor CLIs from npm. Pulling global binaries without checksum verification or pinning can be a supply-chain risk if package registries are compromised.

## Recommendations
- Redact or generalise personal filesystem paths in prompts before sharing publicly.
- Add an explicit security note advising testers to keep API keys out of version control, clear shell history after authentication, and rotate credentials if leakage is suspected.
- Consider pinning CLI versions or verifying package signatures before global installation to mitigate supply-chain attacks, especially when running benchmarks in sensitive environments.
- Document where vendor CLIs persist tokens (e.g., OS keychain, config files) so testers can review permissions and clean up credentials after the benchmark.

## Overall Assessment
The repository itself is low risk because it stores only documentation, but small adjustments to the shared instructions would harden operational security for testers who follow the benchmark.
