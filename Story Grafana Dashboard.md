# Monitor Your Node’s Performance with Grafana and Prometheus

Monitor your node’s performance by installing Grafana and Prometheus. The following script sets up a comprehensive dashboard with essential metrics:

    ansible-playbook install_grafana_prometheus.yml

This script performs the following:

- Installs Grafana and Prometheus.
- Activates metrics collection on the `story-consensus` node.
- Configures a Grafana dashboard with key metrics.

## Accessing the Grafana Dashboard

Access the Grafana dashboard via your server’s IP address on port 3000:

    http://<your_server_ip>:3000

### Login Credentials:

- **Username**: admin
- **Password**: admin

**Note**: Upon your first login, you will be prompted to change the default password for security reasons.
![image](https://github.com/user-attachments/assets/fae8041c-7d97-4e49-a611-14a231100ed0)

## Important Metrics to Monitor

Here are some crucial metrics included in the dashboard:

### Block Height:

- **Description**: Indicates the height of the latest block.
- **Importance**: Confirms your node is properly syncing with the network.

### Number of Peers:

- **Description**: Shows how many peers your node is connected to.
- **Importance**: A higher number can indicate better network connectivity and stability.

### Memory Usage:

- **Description**: Displays the amount of memory allocated on the heap by Go.
-
