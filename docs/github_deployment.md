# GitHub Deployment Notes

## Recommended Plan

1. Use this `github_repository/` folder as the clean public repository root.
2. Keep the original unstandardized `SummaryofKnowledgeBaseData.xlsx` out of the repository.
3. Use PNG versions of Figure 4 to Figure 8 in the README so GitHub can display them directly.
4. Upload high-resolution TIFF files larger than 100 MB through Git LFS or GitHub Releases.
5. Use the included `LICENSE` file for CC BY 4.0 reuse terms.

## Upload as a New GitHub Repository

Run these commands inside `github_repository/`:

```bash
git init
git add .
git commit -m "Initial public release"
git branch -M main
git remote add origin https://github.com/YOUR_ACCOUNT/YOUR_REPOSITORY.git
git push -u origin main
```

Replace `YOUR_ACCOUNT` and `YOUR_REPOSITORY` with your GitHub account and repository name.

## Optional: Add Large TIFF Files with Git LFS

Figure 5 to Figure 8 high-resolution TIFF files are larger than GitHub's normal per-file limit. If you need to include them in the repository, use Git LFS before adding those files:

```bash
git lfs install
git lfs track "*.tif"
git lfs track "*.tiff"
git add .gitattributes
```

Then copy the large TIFF files into `figures/high_resolution/` and commit them:

```bash
git add figures/high_resolution/
git commit -m "Add high-resolution figures with Git LFS"
git push
```

If Git LFS is not available, upload the large TIFF files as GitHub Release assets instead of committing them directly.

## Check Before Pushing

```bash
git status
git ls-files
```

Confirm that `SummaryofKnowledgeBaseData.xlsx`, API keys, PDF full texts, and temporary notebook outputs are not included.
