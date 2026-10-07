# BACK JAMMIN (bgammon)

Status: runs (legacy engine, smoke-tested 2026-10-07). Draws the board and dice; play-test pending.

## Checklist
- [ ] Window size in game.conf matches the largest PNG (notes/scaffold.md)
- [ ] Every symbol in notes/unresolved.txt has a stand-in in src/host/loader_services.cpp
      (`make analyze GAME=bgammon` until it reports 0)
- [ ] First run: `make run GAME=bgammon DEBUG=shots` — crash trace + screenshots in notes/shots
- [ ] Paths: `make run GAME=bgammon DEBUG=files`; engine trace: `mkdir -p data/var/merit/debug/files && touch data/var/merit/debug/files/resource_locator`
- [ ] Reference code: `make decompile GAME=bgammon`
- [ ] Translations + help text appear (gamedata/translations/bgammon.utf8)
- [ ] Sound and music play (`DEBUG=sound`)
- [ ] A full game plays through (`DEBUG=profile` to catch stalls and old-malloc bugs)

## Log
<!-- dated notes: what broke, what fixed it -->

- 2026-10-07 — runs on src/legacy with no stubs; Draws the board and dice; play-test pending.
