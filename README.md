# NWHL Tracking Data

This project takes videos from the (then) NWHL 2021 playoffs that were on Twitch and uses a couple models to determine the coordinates of every player visible in the frame.  These are combined with [event level data](https://github.com/bigdatacup) made available by Stathletes for the 2021 Big Data Cup.

Details on the homography estimation model can be found [here](https://thebucketless.wordpress.com/2022/02/11/player-tracking-a-new-cartographer/).
The multi-object tracker (MOT) is still a work in progress.

While creating annotations for the homography model, it was found that the rink dimensions didn't align with expectations.  This was fixed by adding 5 feet to each side of the neutral zone.  As a result, the model's coordinates don't match up with those provided by Stathletes.  To account for this, the Stathletes coordinates in the offensive zones have been squeezed between the tops of the faceoff circles and the blue lines while the neutral zone gets spread out evenly between red line and blue lines.

Listed IDs for players are intended to reflect distinct players, not the number on the back of their jersey.

As this is still a work in progress, expect flaws with the results.  Notably, multiple goaltenders can appear in the crease due to some foolishness on my part.
