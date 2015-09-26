# role to automatic setup firewall rules for some cluster

nothing but Debian/Ubuntu supported yet

## Variables to be defined

variable name | example | comment
------------- | ------------- | -------
`cluster_group_name` | cassandra | name of the ansible inventory group cluster nodes belongs to. Used to get IPs of the nodes.
`cluster_failovers` | [ { addr: "1.2.3.4/32", port: 80, proto: "tcp" } ]| additional addresses not configured on the nodes directly and must be serverd by the nodes. Very specific for some complicated installations, you can ingnore it in most cases.
`cluster_friends` | ["4.3.2.1", "8.7.6.5"] | addresses are not belogs to cluster directly but have to have the full access to all the nodes. Usually cluster slients.
`cluster_ports` | [ { port: 80, proto: "tcp" } ] | the ports on the clusters dodec must be serverd worldwide
