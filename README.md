# Актёр (Actor)

Track 4 of 7 on «Ностальгия» (_Nostalgiya_, “Nostalgia”), the album by Полуживые (_Poluzhivye_), on poems by Arseny Tarkovsky.

On the site: https://vovazakharov.com/music/actor

## Files

- `actor_mix.mp3` — the mix, unmastered: what the master was made from.
- `actor.mp3` — the master. The mix survives only as an mp3, so the master is one too.
- `mastering/` — the script that made the master: `master.py`, the `spectrum.py` it imports, and their `requirements.txt`.

## How it was mastered

```sh
pip install -r mastering/requirements.txt
python mastering/master.py actor_mix.mp3 ref.flac actor.mp3
```

with `ffmpeg` on `PATH` and the reference below saved as `ref.flac`. Half
strength (`master.py`'s default): Matchering matches the mix to the reference,
half of the EQ difference goes onto the mix, and a limiter keeps the decoded
file under -1 dBTP. `master.py`'s docstring has the whole chain.

## The reference

«Ночной сад» (_Nochnoy sad_, “Night Garden”), Полуживые, at [vovas-music/sad@34d860b](https://github.com/vovas-music/sad/blob/34d860bc22425910efaaa654e3e0b8f901064129/Poluzhivye%20-%20Nochnoy%20sad.flac) — raw download:
https://raw.githubusercontent.com/vovas-music/sad/34d860bc22425910efaaa654e3e0b8f901064129/Poluzhivye%20-%20Nochnoy%20sad.flac

It was picked blind: three catalogue masters each mastered the mix, and the
operator ranked them unlabelled, loudness-matched, before learning which was
which. It is linked rather than copied here, since it already lives in this
organization.
