# distance-vector-routing
Virtual network on top of UDP, in which each UNIX process will be a node. Network will update itself. Implemented with C in Linux.

**Protocol:**
![GitHub Logo](/protocol.png)


To run:(Remember to make first)(*Not finished*)
``rt -n <node_id> [-f <scenario_file>] [-u update-time] [-t time-between-event-sets] [-v]``

The -n option is mandatory and specifies the node id.
the optional -f parameter specifies a scenario file (default config).
the optional -t parameter specifies how long to wait between executing event sets (default 30 seconds).
The -u option specifies how long to wait (in seconds) before sending out distance vector updates; this should default to 3 seconds.
If the -v (verbose) option is **not present**, to stdout: 
  1) each event in the event set that it acts upon using print event, 
  2) the routing table entry after it was changed in response to processing a routing update using print rte 
  3) the full routing table after dispatching the entire event set using print rt.
If the -v option **is present**, then the full routing table should additionally be printed after processing
every routing update (whether or not it changed any entries) using print rt.
