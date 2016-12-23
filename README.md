# SDN-Layer-3-Routing

A Software Defined Networking layer-3 routing application that constructs route tables based on a
global view of the network topology.  The appropriate route table is installed in each SDN switch by
the application, and each SDN switch will forward packets according to the installed route table.

This layer-3 routing application installs route table entries that match packets based on their
destination IP address (and Ethernet type), and execute an output action to send the packet out a
specific port on the SDN switch.  Traffic is forwarded to the intended host using the shortest path.
We use the Bellman-Ford algorithm to compute the shortest paths to reach a host from every other
host.
