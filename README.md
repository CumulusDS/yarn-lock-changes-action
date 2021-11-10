[![Create Release][release-badge]][release-url]
[![Import Labels][import-labels-badge]][import-labels-url]
[![Sync Labels][sync-labels-badge]][sync-labels-url]
[![PR AutoLabeler][autolabeler-badge]][autolabeler-url]
[![Assigner][assigner-badge]][assigner-url]

Description

### Inputs
#### `token`
Repository GITHUB_TOKEN which allows action to make calls to the GitHub API
Required.

#### `collapsibleThreshold`
Number of lock changes, which will result in collapsed comment content and an addition of changes summary table
Default: `25`

#### `failOnDowngrade`
When a dependency downgrade is detected, fail the action. Comment will still be posted
Default: `false`

#### `path`
Path to the yarn.lock file in the repository. Default value points to the file at project root
Default: `yarn.lock`

#### `updateComment`
Update the comment on each new commit. If value is set to false, bot will post a new comment on each change
Default: `true`


### Example usage
```yaml
      - name: Yarn Lock Changes
        uses: CumulusDS/yarn-lock-changes-action@v1
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```



[release-badge]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/release.yml/badge.svg
[release-url]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/release.yml
[import-labels-badge]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/labels_import.yml/badge.svg
[import-labels-url]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/labels_import.yml
[sync-labels-badge]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/labels_sync.yml/badge.svg
[sync-labels-url]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/labels_sync.yml
[autolabeler-badge]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/autolabeler.yml/badge.svg
[autolabeler-url]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/autolabeler.yml
[assigner-badge]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/assign.yml/badge.svg
[assigner-url]: https://github.com/CumulusDS/yarn-lock-changes-action/actions/workflows/assign.yml
