# Dynatrace Host Monitoring Mode – README

This guide explains **three simple ways** to change **Host Monitoring Mode** in Dynatrace.
It is written for beginners and works for real production environments.

---

## Prerequisites (Common for All Methods)

You need only:

* Dynatrace SaaS Environment URL
  Example: `https://abc12345.live.dynatrace.com`
* API Token with permissions:

  * Read entities
  * Read settings
  * Write settings
* Command line access (PowerShell / Terminal)

---

## Way 1: Host-by-Host Using HOST IDs (Manual Method)

**Use when:** Few hosts, one-time change

### Simple Explanation

You first fetch HOST IDs from Dynatrace, then explicitly set monitoring mode for each host using the API.

### Steps (High Level)

1. Get HOST IDs using `/api/v2/entities`
2. Create a JSON file with HOST IDs
3. Call Settings API to set `INFRASTRUCTURE` mode

### Pros

* Direct control per host

### Cons

* ❌ Manual effort
* ❌ Not scalable for many hosts
* ❌ New hosts not auto-covered

---

## Way 2: Host Group / Tag-Based Rule (BEST PRACTICE ⭐)

**Use when:** 10+ hosts, cloud, auto-scaling environments

### Simple Explanation

Instead of configuring each host, you tag hosts and create **ONE rule** that applies Infrastructure mode to all of them.

### Steps (High Level)

1. Assign a tag or host group to hosts (example: `env:infra-only`)
2. Create one monitoring mode rule targeting that tag

### Pros

* ✅ One rule for all hosts
* ✅ New hosts auto-covered
* ✅ Easy rollback
* ✅ Enterprise-ready

### Cons

* Slight initial setup

---

## Way 3: User Gives Host Names (Safest Real-World Method)

**Use when:** Users provide only server names (not HOST IDs)

### Simple Explanation

You tag hosts using their **names**, then apply one monitoring rule to tagged hosts.
Dynatrace automatically matches names internally.

### Steps (High Level)

1. Put host names in a file (example: `hosts.txt`)
2. Tag hosts using `entityName()` selector
3. Apply one Infrastructure monitoring rule

### Pros

* ✅ No HOST IDs needed
* ✅ No copy-paste mistakes
* ✅ Safe (wrong name = no change)
* ✅ Clean rollback

### Cons

* Requires tagging step

---

## Quick Comparison

| Method                 | Effort | Scales | Auto for New Hosts |
| ---------------------- | ------ | ------ | ------------------ |
| Host by Host           | ❌ High | ❌ No   | ❌ No               |
| Host Group Rule        | ✅ Low  | ✅ Yes  | ✅ Yes              |
| Host Name → Tag → Rule | ✅ Low  | ✅ Yes  | ✅ Yes              |

---

## Final Recommendation

* **1–2 hosts / testing:** Way 1
* **Production / large setup:** Way 2
* **User gives host names:** Way 3 (Best & safest)

---

## Interview One-Liner

> “We avoid per-host configuration. We use tag-based Dynatrace Settings API rules to enforce host monitoring mode for scalability, safety, and auto-coverage.”

---

## Notes

* Always verify tagging before applying rules
* Prefer tag-based rules to avoid configuration drift
* Rollback = remove rule or remove tag

---

**End of README**
