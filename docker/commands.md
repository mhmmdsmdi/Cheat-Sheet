# Docekr Commands

## Rebase

```sh
git rebase branch-1(base) branch-2(feature)
```

branch-1 : برنچی که قرار است از روی آن الگو برداشته شود
branch-2 : برنچی که قرار است الگو روی آن قرار بگیرد

Example:

```sh
git rebase master stuff-features`
```

## Save , Load | Copy docker images to other host

Save the Docker image as a tar file:

```sh
docker save -o <path for generated tar file> <image name>
```

Load the image into Docker:

```sh
docker load -i <path to image tar file>
```