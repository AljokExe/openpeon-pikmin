<img src="icons/pack.png" alt="A Red Pikmin" width="96" align="right">

# Pikmin for OpenPeon

A sound pack of 35 Pikmin sounds for AI coding agents. A Pikmin cheers when a
session starts, carries treasure home when a task is done, and perishes when a
task fails.

The pack follows [CESP](https://github.com/PeonPing/openpeon) (the Coding
Event Sound Pack standard) from OpenPeon. It is listed in the
[OpenPeon registry](https://openpeon.com/packs/pikmin), so
[peon-ping](https://github.com/PeonPing/peon-ping) and any other CESP player
can install it by name.

## Install

With [peon-ping](https://github.com/PeonPing/peon-ping) installed:

```sh
peon packs install pikmin
peon packs use pikmin
```

To try a local copy, for example a change before a release:

```sh
peon packs install-local ./openpeon-pikmin
peon packs use pikmin
```

## Sounds

`openpeon.json` maps each sound to a CESP event. A player picks one sound at
random from the event's list.

| Event | Sounds | For example |
|---|---|---|
| `session.start` | 8 | "Pikmin!", a Pikmin plucked from the ground |
| `task.acknowledge` | 4 | "Hyah!", a Pikmin thrown |
| `task.complete` | 7 | a Pikmin carries treasure, "Phew!" |
| `task.error` | 11 | a Pikmin perishes: burnt, drowned, shocked |
| `input.required` | 9 | Olimar's whistle, Louie's whistle |
| `resource.limit` | 4 | the clock, a boss appears |

## Release

1. Change `openpeon.json` and the files in `sounds/`.
2. Raise `version` in `openpeon.json`.
3. Tag the commit with the same version, for example `v1.2.0`, and push the tag.
4. Open a pull request on [PeonPing/registry](https://github.com/PeonPing/registry)
   that points the `pikmin` entry at the new tag.

## Licence

The pack is shared under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/),
as `openpeon.json` says. The sounds come from the *Pikmin* games, which belong
to Nintendo. This is a non-commercial fan pack, and it is not made or endorsed
by Nintendo.
