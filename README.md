# JRA free launcher

This repository contains launcher configuration only. Collector source and all
captured source HTML, CSV and JSON remain in a separate private repository.
No betting, model training, or changes to racing analysis rules are performed.

Place free-capture.yml at .github/workflows/free-capture.yml.
Use standard ubuntu-24.04 runners. No payment method, paid runner, public artifact
upload, server subscription or public data endpoint is required by this design.

The owner must configure the repository secret JRA_DATA_TOKEN with a fine-grained
token limited to the private YONG3777/jra-odds repository, Contents read/write.
Never paste the token in an issue, workflow file, README or chat.

Run check first, then discover. These are not proof of real timed collection.
Set the Actions variable COLLECT_ENABLED=true only after access and private
publication have been verified. It is inactive by default.

Scheduled starts (JST): 06:47, 10:47, 13:47. Target windows: before 12:30,
12:30–16:00, 16:00–18:00. Early startup reduces delay exposure but cannot guarantee
startup, exact receipt time or zero missing observations. GitHub can delay or drop
scheduled runs, and can disable schedules in inactive public repositories.

Only workflow_dispatch and schedule are accepted; no external PR code or arbitrary
repository/ref input is executed. The private source revision is pinned.

Target races are selected through private selection.json. An empty or outdated
selection never expands to all races. No target race list is published here.
