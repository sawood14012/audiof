# Identify what's playing




## How to set up 

1. Run `$ make clean reset` to clean & init database struct
1. Run `$ make tests` to make sure that everything is properly configurated
1. Copy some `.mp3` audio files into `mp3/` directory
1. Run `$ make fingerprint-songs` to analyze audio files & fill your db with hashes
1. Start play any of audio file (from any source) from `mp3/` directory, and run (parallely) `$ make recognize-listen seconds=5`



## How to
- To remove a specific song & related hash from db

  ```bash
  $ python sql-execute.py -q "DELETE FROM songs WHERE id = 6;"
  $ python sql-execute.py -q "DELETE FROM fingerprints WHERE song_fk = 6;"
  ```

