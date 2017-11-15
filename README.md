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
python3 -m venv . 
source bin/activate
pip install ovh pyyaml
```

## Configuration

### Create OVH token

Grab application key and application secret from:

https://api.ovh.com/createApp

Note: `ovh-redirections` will request a consumer key itself, if you want to manage permissions yourself, use:

https://api.ovh.com/createToken

### Set credentials

```
cp ovh-redirections.yaml.sample ~/.config/ovh-redirections.yaml
vim ~/.config/ovh-redirections.yaml
```

Note: you must set domain, endpoint, application key and application secret. If you don't have consumer key `ovh-redirections` will request it from OVH.

## Quick start

### Fetch

Fetch redirections list with details, sort and group them then write them to an
hidden file `.example.com_ovh-redirections.yaml`. *This file should not be
edited*

```
./ovh-redirections fetch
```

### Checkout

Copy previously fetched redirections file to a editable file named
`example.com_ovh-redirections.yaml`.

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

## Other useful related applications

https://github.com/ovh/ovh-cli
