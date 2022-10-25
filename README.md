# dictpress

dictpress is a free and open source, single binary webserver application for building and publishing fast, searchable dictionaries for any language.

Examples dictionaries:
- [Alar](https://alar.ink/) — Kannada-English dictionary.
 - [Olam](https://olam.in/) — English-Malayalam, Malayalam-Malayalam dictionary.


## Features
- Build dictionaries for any language to any language.
- Supports multiple dictionaries and languages in the same database.
- Custom themes and templates for publishing dictionary websites.
- Paginated A-Z (all alphabets for any language) glossaries.
- HTTP/JSON API for search and everything else.
- Pluggable search algorithms, eg: fulltext search, phonetic word search etc.
- Admin UI for managing and curating dictionary data.
- Admin moderation UI for crowd sourcing dictionary entries.
- Bulk CSV to database import.



[![image](https://user-images.githubusercontent.com/547147/175945746-575c2cb7-7478-414a-93ae-014196d3385d.png)](https://olam.in)
[![image](https://user-images.githubusercontent.com/547147/175945847-40d3ae1c-c81a-4283-94af-9299476bfd7f.png)](https://dict.press/static/admin.png)

## Getting started
- [Download](https://github.com/knadh/dictpress/releases) the latest version.
- [Read the docs](https://dict.press) for setup and usage instructions.

## Develop with Docker
You can follow these commands to set up a quick development environment using
Docker. Please note that this is to speed up development and demos, not for
production use.

The only thing included in the Docker Compose file is a Postgres service, but
combined with the dictpress option `--new-pgenv`, it helps you skip the
task of manually setting up and linking a Postgres instance.

After cloning the repo and entering it's directory:

```
make dist
./dictpress --new-pgenv --new-config
docker compose up -d
# wait for a couple of seconds
./dictpress --install
```

Now you can run `dictpress` as usual:

```
./dictpress
```
