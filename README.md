# b2restic

A minimal, opinionated script to manage restic back-ups on a Backblaze B2 bucket. 

## Installation

Download the script as follows:

```bash
curl -o b2restic https://raw.githubusercontent.com/daberg/b2restic/main/b2restic
chmod +x b2restic
```

## Configuring

Set up the necessary environment variables. The `template.env` can be used for convenience:

```bash
curl -o .env https://raw.githubusercontent.com/daberg/b2restic/main/template.env
chmod 400 .env
vim .env
```

## Running

Init the repo:

```bash
b2restic init
```

Back up a folder and prune outdated snapshots:

```bash
b2restic backup /path/to/folder
```

List snapshots:

```bash
b2restic list
```

Mount the repo to a folder:

```bash
b2restic mount /path/to/mount/point
```

## License

MIT License
