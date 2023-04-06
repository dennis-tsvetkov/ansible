![](https://kafka.apache.org/logos/kafka_logo--simple.png)
#  Apache Kafka role
The simple role to deploy cluster of Kafka brokers.
Current version is 3.4.0, KRaft based, Zookeeper is not used.
### How to use
- Put list of your broker hosts into a group in the `inventory` file.
- Assign them `node_id`'s and mark at least 3 of them with `is_controller=true` (See [inventory.example](https://raw.githubusercontent.com/dennis-tsvetkov/ansible/master/inventory.example) for reference)
- Put the same group name into the `kafka_hosts` variable in `group_vars/<your_group>`
- Put the same group name into the `hosts` variable in `playbooks/kafka.yml`
- Deploy the role in a usual way with `ansible-playbook -i inventory playbooks/kafka.yml`
