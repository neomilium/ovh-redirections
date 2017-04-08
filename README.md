# ovh-redirections

Do not get crazy to handle OVH redirections anymore !

## Features

* Fetch redirections list and write it as YAML file
* Edit with your favorite app a YAML file to add / delete redirection(s)
* Apply all modifications in one command

## Installation

```
git clone https://github.com/neomilium/ovh-redirections.git
cd ovh-redirections
```

```
python3 -m venv
source bin/activate
pip install ovh pyyaml
```

## Configuration

```
cp ovh-redirections.yaml.sample ~/.config/ovh-redirections.yaml
vim ~/.config/ovh-redirections.yaml
```

## Quick start

### Fetch

Fetch redirections list with details, sort and group them then write them to a file.

```
./ovh-redirections fetch
```

*This file should not be edited*

### Checkout

Copy previously fetched redirections file to a editable file named *example.com_ovh-redirections.yaml*

```
./ovh-redirections checkout
```

### Edit redirections

Now, you have to edit your file according to your will.

### Diff

Compares edited file with fetched one.
It will show *added* and *deleted* redirections.


```
./ovh-redirections diff
```

### Commit

Apply added / deleted redirections online.

```
./ovh-redirections commit
```
