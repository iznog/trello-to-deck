# trello-to-deck
> Move to the bright side!

trello-to-deck reads from an JSON export of Trello and creates a board in [Nextcloud Deck](https://apps.nextcloud.com/apps/deck).

## Installation

```
pip install .
```

## Usage example

Simply invoke the CLI tool `trello-to-deck`:

```console
# trello-to-deck
usage: trello-to-deck [-h] input_json nextcloud_instance username password
trello-to-deck: error: the following arguments are required: input_json, nextcloud_instance, username, password
```

You have to provde the arguments `input_json` e.g. `trello.json`, `nextcloud_instance` e.g. `https://example.org/nextcloud` and the `username` and `password` for nextcloud. If you have 2-FA please create a temporary app passowrd for converting to Deck.

## What is migrated?

* Labels
* Stacks
* Cards
* Checklists (yes they are supported by Deck!)
* Due-date
* Order of Stacks, Cards, Checklists etc.

## MUST READ: What is NOT migrated?

* Creating archived cards
  I have over 2000 archived cards in my personal Trello. Right now Deck can not handle this amount. Therefore currenlty no archived cards are migrated!
* Assigning the correct people on the cards. Only the creating account is assigned right now.
* Attachments
