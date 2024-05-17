# Clone Github Repository Action

### For a public repository (with depth)

```bash
- name: Clone GuillaumeFalourd/poc-github-actions PUBLIC repository
  uses: GuillaumeFalourd/clone-github-repo-action@v2.3
  with:
    depth: 1
    branch: 'main'
    owner: 'GuillaumeFalourd'
    repository: 'poc-github-actions'
```

### For a private repository

To use this action to clone a `PRIVATE` repository the Github User/Admin has access to, it's necessary to create a [PERSONAL ACCESS TOKEN](https://github.com/settings/tokens) with `REPOSITORY` scopes.

```bash
- name: Clone GuillaumeFalourd/formulas-training PRIVATE repository
  uses: GuillaumeFalourd/clone-github-repo-action@v2.3
  with:
    owner: 'GuillaumeFalourd'
    repository: 'formulas-training'
    access-token: ${{ secrets.ACCESS_TOKEN }}
```

### Access repository content

After using this action in your workflow, you can use the following command to access the cloned repository content:

```bash
cd <repository-name>
```

#### Step Example

```bash
- name: Access cloned repository content
  run: |
    cd <repository-name>
    ls -la
```

## Licensed

☞ This repository uses the [Apache License 2.0](https://github.com/GuillaumeFalourd/aws-cliaction/blob/main/LICENSE)

## Forked from - Original

<https://github.com/GuillaumeFalourd/clone-github-repo-action>
