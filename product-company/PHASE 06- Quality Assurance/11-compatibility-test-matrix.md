# compatibility-test-matrix.md

> **Skill:** Produces a browser and device compatibility test matrix documenting supported combinations, test results by combination, known issues, and the compatibility quality gate status for release.

---

## TLDR

A compatibility test matrix documents which browser/OS/device combinations are officially supported, test results for each, known issues per combination, and the quality gate status for the release. It prevents the common scenario: a release that works perfectly in Chrome on macOS but is broken in Safari on iOS or Firefox on Windows.

---

## Topic Explanation

### Support Tiers Based on Product Analytics

Not all browser/device combinations can or should be tested equally. Support tiers provide a structured framework:

**Tier 1 (Fully Supported, all issues block release):** Combinations used by the majority of users. Determined from actual product analytics. A Tier 1 combination with any critical path failure blocks the release.

**Tier 2 (Supported, issues are high priority):** Significant but less common combinations. Issues are high priority but may not block the release depending on severity.

**Tier 3 (Best effort):** Minor browser versions, older OS versions, niche devices. Known issues are logged but do not block release.

The tier structure must be derived from the product's own analytics data, not from industry browser market share statistics. If 40% of this product's users are on Safari iOS, it must be Tier 1 regardless of industry market share figures.

### Browser Engine Coverage

For web applications, testing must cover all three major rendering engines regardless of brand:

**Chromium engine:** Chrome, Edge, Brave, Opera
**Gecko engine:** Firefox
**WebKit engine:** Safari (macOS and iOS), all iOS browsers

Testing only Chrome misses 30 to 40% of users on different rendering engines, even if Chrome has the highest market share.

### Responsive Viewport Testing

Standard viewports to test for web applications:
- 375px width: mobile small (iPhone SE)
- 390px width: iPhone 14 / modern mid-size iPhone
- 412px width: typical Android phone
- 768px width: tablet portrait
- 1024px width: tablet landscape
- 1280px and 1440px: standard desktop

---

## Output Format

```
1. MATRIX HEADER
   Release version, test date, QA lead.
   Analytics period used to determine support tier assignments.

2. SUPPORTED COMBINATIONS BY TIER

   TIER 1 (fully supported, must pass):
   Browser | Version | OS | Device type | User % from product analytics

   TIER 2 (supported, should pass):
   Browser | Version | OS | Device type | User % from product analytics

   TIER 3 (best effort):
   Browser | Version | OS | Device type

3. TEST RESULTS MATRIX
   For each Tier 1 and Tier 2 combination:
   Browser/Device | Version | OS | Core features | Visual render | Forms | Performance | Overall | Issue IDs

4. KNOWN ISSUES BY COMBINATION
   For each known issue:
   - Issue ID and title
   - Affected combination(s)
   - Severity
   - User impact
   - Workaround if available
   - Status: open / fix committed / accepted risk

5. CRITICAL PATH RESULTS
   Results for the most critical user journeys verified across all Tier 1 combinations.
   Any critical path failure is a blocking issue regardless of which tier.

6. RESPONSIVE / VIEWPORT TESTING
   Results at standard viewport widths.
   Known layout or functional issues at specific breakpoints.

7. COMPATIBILITY QUALITY GATE

   PASS: All Tier 1 combinations pass all critical paths. No critical issues in Tier 2.

   CONDITIONAL PASS: [specific conditions, e.g., one Tier 2 issue with an accepted workaround]

   FAIL: One or more Tier 1 combinations fail a critical path.
   Blocking issues: [list specific combination and issue]
```

---

## Starter Prompt

```
You are a QA engineer producing a compatibility test matrix.

Product type: [web app / mobile app / desktop]
Product analytics: [browser and device breakdown from the product's own analytics]
Test combinations covered: [what was actually tested]
Test results: [pass/fail by combination]
Known compatibility issues: [issues found during testing]
Critical user journeys tested: [the key flows verified across combinations]

Produce a complete compatibility test matrix with support tiers derived
from the product analytics, full results matrix, known issues detail, and quality gate verdict.
Any Tier 1 combination with a failing critical path is always a blocking issue.
```

---

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
