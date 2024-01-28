# GitHub Action: Delete tag and release

Fork of the original that updates to Node 20.

---

Add the following step to your workflow:

```yaml
- uses: ClementTsang/delete-tag-and-release@v0.3.1
  with:
    delete_release: true # default: false
    tag_name: v0.1.0 # tag name to delete
    repo: <owner>/<repoName> # target repo (optional). defaults to repo running this action
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
