# Context Handoff

**Last updated:** 2026-02-01
**Session:** Folder restructure + ZFU cleanup

---

## Lecture Details

| Field | Value |
|-------|-------|
| Date | **Saturday Feb 7, 2026** |
| Time | 13:00 - 16:45 (3.75 hours) |
| Audience | Financial services executives (CAS AI in Finance) |
| Location | HWZ, Zurich |
| Second session | **Saturday Apr 25, 2026** — "AI und Deep Tech Future Outlook" |
| Material due | Wednesday Feb 5 |
| Student email | Monday Feb 3 |

---

## Current Status

**Folder structure migrated to unified timeline.** READMEs updated. ZFU references removed from current files.

### New Structure: `segments/`

```
2026_02_07_AIF/segments/
├── 01-how-i-built-this-lecture/
├── 02-technology-revolution-lecture/
├── 03-writing-profile-exercise/
├── 04-ai-managerial-skill-lecture/
├── 05-company-research-exercise/
├── 06-information-overload-lecture/
├── 07-second-brain-exercise/
├── 08-cognitive-limits-lecture/
└── 09-demo-personalized-summary-lecture/
```

Each segment folder contains:
- **Lectures:** `script.md` + `gamma-prompt.md`
- **Exercises:** `README.md` + step-by-step guides

### Changes Made This Session

1. ✅ Migrated `slides/` and `exercises/` → unified `segments/` folder
2. ✅ Renamed folders with delivery sequence numbers + type suffix
3. ✅ Updated both READMEs with new structure
4. ✅ Removed ZFU references from `.gitignore`, `README.md`, `BUILD_LOG.md`

---

## Outstanding: ZFU Git History Purge

**Status:** ZFU folder deleted, references removed from current files.

**Problem:** Commit `1e489ce` still contains `2026-02_ZFU/ZFU_Project_Brief.md` in git history. Anyone with repo access can recover it.

**Solution:** Run `git filter-repo` to rewrite history:
```bash
pip install git-filter-repo
git filter-repo --path 2026-02_ZFU/ --invert-paths
git push --force
```

**Impact:**
- Requires force-push
- All collaborators must re-clone
- GitHub will eventually garbage-collect the orphaned commits

**Decision needed:** Proceed with history rewrite? (Recommended: yes, if ZFU content is truly confidential)

---

## Resume Instructions

1. If ZFU purge approved → run `git filter-repo` commands above
2. Commit current changes (folder restructure)
3. Force-push to origin

---

## Timeline

- ✅ Friday Jan 31: Lecture content built
- ✅ Saturday Feb 1: Folder restructure
- Monday Feb 3: Student prereq email
- Wednesday Feb 5: Materials to HWZ
- Saturday Feb 7: Lecture delivery
