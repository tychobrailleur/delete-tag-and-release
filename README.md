# GitHub Action: Delete tag and release

Fork of the original that updates to Node 20.

**Note**: You may be able to skip using this if you are working on a GitHub-hosted runner,
or you can install the `gh` tool, as `gh` now natively [can delete releases](https://cli.github.com/manual/gh_release_delete).
For example:

```yaml
      - name: Delete tag
        run: gh release delete $TAG --cleanup-tag
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

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
