# Validator Utilities Script

I included the `validator_utils.sh` script, offering essential utilities for node management.

## Backing Up and Restoring Validator Keys

### Backup Keys:

To back up your validator keys, use:

```bash
./validator_utils.sh backup_keys
```

This command backs up your validator keys, including:

- **EVM Private Key**: Located at `/root/.story/story/config/private_key.txt`
- **Tendermint Validator Key**: Located at `/root/.story/story/config/priv_validator_key.json`

The backup is saved at:

```
/root/backup-keys-story/story_keys_backup.tar.gz
```

After running the backup command, you’ll see:

```
Backup created at /root/backup-keys-story/story_keys_backup.tar.gz
```

This backup contains:

- EVM private key (from `/root/.story/story/config/private_key.txt`)
- Tendermint validator key (from `/root/.story/story/config/priv_validator_key.json`)

**Note**: Keeping these keys safe is crucial for node recovery and security.

### Restore Keys:

To restore your validator keys from the backup archive, use:

```bash
./validator_utils.sh restore_keys
```

This is very useful if you change servers.

## Checking Node Synchronization Status

To check your node’s current block height, use:

```bash
./validator_utils.sh sync
```
![image](https://github.com/user-attachments/assets/158099d8-de69-458c-81be-81eee7ad773d)

## Viewing Validator Information

To get detailed information about your validator, including the catching up status (whether the node is still syncing), use:

```bash
./validator_utils.sh info
```
![image](https://github.com/user-attachments/assets/bad84d6f-3c8e-4ca1-803b-756570c47858)

This command provides:

- **Node ID**
- **Moniker**
- **Network**
- **Catching Up Status**: Indicates if the node is still syncing (`true`) or fully synced (`false`).
