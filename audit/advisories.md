# Dependency Security Audit — Most Severe Reviewed Advisories

Review run on **2026-10-21 (UTC)** against GitHub's reviewed global security advisories (npm ecosystem). One entry per audited package: the most severe *reviewed* advisory affecting it, with GHSA id, severity, a plain-English summary, and the first patched version where one is listed.

---

## lodash

- **GHSA ID:** `GHSA-jf85-cpcp-j695`
- **Severity:** Critical (CVSS 9.1)
- **Description:** The `defaultsDeep` function allows an attacker to pollute `Object.prototype` by passing `{constructor: {prototype: {...}}}`, adding or modifying properties on every object.
- **First patched version:** 4.17.12

## qs

- **GHSA ID:** `GHSA-hrpp-h998-j3pp`
- **Severity:** High (CVSS 7.5)
- **Description:** Parsing a crafted query string containing an `__proto__` key lets an attacker pollute `Object.prototype`, which can hang or crash the Node process.
- **First patched version:** 6.10.3 (with per-release backports down to 6.2.4)

## minimatch

- **GHSA ID:** `GHSA-7r86-cg39-jmmj`
- **Severity:** High (CVSS 7.5)
- **Description:** Glob patterns with multiple non-adjacent `**` segments cause combinatorial backtracking in `matchOne()`, stalling the Node event loop for seconds per call (denial of service).
- **First patched version:** 10.2.3 (per-major backports: 9.0.7, 8.0.6, 7.4.8, 6.2.2, 5.1.8, 4.2.5, 3.1.3)

## elliptic

- **GHSA ID:** `GHSA-vjh7-7g9h-fjfh`
- **Severity:** Critical
- **Description:** Signing a single malformed message (for example a string rather than a Buffer) reuses the ECDSA nonce `k`, allowing full private key extraction from the resulting signature pair.
- **First patched version:** 6.6.1

## node-fetch

- **GHSA ID:** `GHSA-r683-j2x4-v87g`
- **Severity:** High (CVSS 8.8)
- **Description:** Secure headers such as `authorization`, `www-authenticate`, `cookie`, and `cookie2` are forwarded to untrusted sites when node-fetch follows a redirect.
- **First patched version:** 3.1.1 (v3 line) / 2.6.7 (v2 line)
