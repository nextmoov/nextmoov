# use private git repository as dependency

## add to package.json

example:

```bash
yarn add git+ssh://git@bitbucket.org:nextmoov/smb-pto-lib-backend.git
```

this adds automatically in `package.json`

```json
{
  "dependencies": {
    "smb-pto-lib-backend": "git+ssh://git@bitbucket.org:nextmoov/smb-pto-lib-backend.git"
  }
}
```

Note: maybe a problem if ssh key has a passphrase

## update

If `smb-pto-lib-backend.git` evolves, it will not be automatically updated. To force it, add it again

```bash
yarn add git+ssh://git@bitbucket.org:nextmoov/smb-pto-lib-backend.git
```

## depend on a specific tag/branch

add `#[branch | tag | commit id]` to repository url. For instance, to depend on branch _develop_:

```bash
yarn add git+ssh://git@bitbucket.org:nextmoov/smb-pto-lib-backend.git#develop
```

by tagging correctly our dependencies projects with a version number and specifying tag version in url, we should have something working out of the box, and we can avoid using git submodules.