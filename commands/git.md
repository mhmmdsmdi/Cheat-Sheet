# Docekr Commands

## Rebase

```sh
git rebase branch-1(base) branch-2(feature)
```

branch-1 : برنچی که قرار است از روی آن الگو برداشته شود
branch-2 : برنچی که قرار است الگو روی آن قرار بگیرد

Example:

```sh
git rebase master stuff-features
```

## Sync remotes with local

```sh
git fetch --prune
```

## Merge some repositories to one repository with all unrelated histories

میخواهیم چند Repository مختلف را در یک Repository ادغام کنیم به طوری که تمام تاریخچه های آنها هم موجود باشد.

در ابتدا Repository نهایی را ایجاد و بر روی و آنرا Clone میکنیم

### First Way

```sh
git remote add --f common https://git.kamandsoft.ir/kamandRoot/kamand-common.git

git fetch common

git merge domain/master --allow-unrelated-histories
```

### Second Way (Recomended)

```sh
git subtree add --prefix=<directory-name> <repository-uri> <repository-branch-name>
```

Example:

```sh
git subtree add --prefix=Common https://git.kamandsoft.ir/kamandRoot/kamand-repository.git master
```
