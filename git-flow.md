# Simple Git Flow Guide

## **Branches**

```
main        → always stable, production-ready
dev         → main integration branch (optional)
feature/*   → new features or tasks
bugfix/*    → fixes during development
hotfix/*    → urgent production fixes
release/*   → preparing a new version
```

---

## **Basic Workflow**

### **1. Create a feature**

```
git checkout dev  
git checkout -b feature/<issue-number>-<short-description>
```

### **2. Commit work**

> See commits document: [commits.md](commits.md)

### **3. Push the branch**

```
git push -u origin feature/<issue-number>-<short-description>
```

### **4. Open a Pull Request**

* Target: `dev`
* Add: `Fixes #ISSUE` in PR description
* Merge after approval

---

## **Release Workflow**

```
git checkout dev
git checkout -b release/X.Y.Z
```

* final polishing
* update docs/version

Merge into both:

* `main` → tag release
* `develop` → sync back

---

## **Hotfix Workflow (urgent production fix)**

```
git checkout main
git checkout -b hotfix/X.Y.Z-hotfix-description
```

Fix → merge into:

* `main` (deploy)
* `develop` (sync)

Tag new patch release.

---

## **Branch Naming Examples**

```
feature/42-user-auth
bugfix/103-login-error
release/1.4.0
hotfix/1.4.1-cors-issue
```
