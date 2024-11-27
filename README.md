# Cloud Autotesting

## Setup
Visit [http://scrimmage.csail.mit.edu/], sign in with your credentials. Then, visit [http://scrimmage.csail.mit.edu/autotest_access_key] and copy the string that you are given. Then run:
```
autotest-setup PASTE_IN_THE_STRING_HERE
```

## Usage
The autotest scripts `autotest-run` and `autotest-prun` take the following as arguments:

```
{blitz,regular,long} num_games player1 player2 ...
```

Regular time control is the standard 120+2 that will be used for the exhibition tournament. Each of the players is the name of a leiserchess binary in the current folder. It is a good idea to have a naming convention to your binaries as names must be unique. num_games is the amount of games each binary will play. Therefore, the number of total games will be the number of players times num_games. Please do not spawn too many games!

Finally, autotest-list will list all of the binaries you have uploaded thus far.

**Important**: You may pause autotests that are unnecessary on the scrimmage server: `scrimmage.csail.mit.edu/autotest`.

**Important 2**: the `autotest-run` command does not allow you to upload many a player with the same name multiple times. If you run, `autotest-run regular 1 player1 player2`, it will look for the binaries player1 and player2 in your working directory. Then, it will try to upload them to the scrimmage server. If you have already uploaded a binary with the same name before, it will not reupload it, but rather reuse the older one to run the game. Therefore, I recommend that you have a special directory with your binaries where you can give them special names and you can run games against older binaries.

**Important 3**: the `autotest-run` command is fairly verbose, so you should always carefully read its output.
