# Providing Snapshot Download and Import Service

To help users quickly synchronize their nodes, I developed the `snapshot_manager.sh` script. This script allows you to download and import snapshots of both the `geth` and `story-consensus` nodes, significantly reducing sync time compared to starting from scratch.

## Using the Snapshot Manager

### Downloading a Snapshot

To download a snapshot, use:

    ./snapshot_manager.sh download <type>

Replace `<type>` with either `pruned` or `archive`:

- **Pruned**: A snapshot that contains only the most recent state, resulting in smaller size.
- **Archive**: A complete snapshot with full historical data.

Example:

    ./snapshot_manager.sh download pruned

This command downloads both the `geth` and `story-consensus` snapshots of the specified type. You will find your snapshot in this folder: `/root/snapshots`.

### Importing a Snapshot

After downloading, import the snapshot to your node:

    ./snapshot_manager.sh import <type>

Use the same `<type>` you used for downloading.

Example:

    ./snapshot_manager.sh import pruned

This command performs the following:

1. Stops the Story services.
2. Imports the downloaded snapshots for both `geth` and `story-consensus`.
3. Restarts the services.

**Note**: This functionality allows your node to catch up with the network quickly and efficiently.

Powered by TRTtheSalad
