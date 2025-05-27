Building the [platform_description](https://github.com/eclipse-score/process_description) documentation, that is heavily linked with 'score_platform'

The two possible ways are 'latest' as well as 'release'. 

Latest => Linking to the latest 'main' branch. This grabs the 'needs.json' from the specified URL.  
Release => Depends on the latest released version of imported Module. Builds the 'needs.json' in Bazel as prerequisite.


# Bazel Module One-Directional Linking 

**Date:** 27.05.2025

---

## 1. The Problem
Due to the splitting of 'score' into multiple repositories, there was no of getting all needed documentation, as cross links still existed.  
Or in other words:
- No way to reference or navigate between documentation of referenced modules
- Proxy setups would fail, due to sphinx-needs not respecting proxies apparently

---

## 2. The Solution 

### What We Implemented
`docs-as-code` has been build to solve this issue. We now (in v0.2.6) integrated a way to reference release and latest versions of another bazel module.

This enables us to do the following things:
- One-directional linking system between Bazel modules
- Integrated documentation links through sphinx
- Seamless navigation from module to module


---

## 3. Solution in action

![demo](demo.gif)

---

