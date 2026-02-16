# Vitaliy Guschin

System & Network Software Engineer focused on C/C++ development, networking protocols, and OS internals.

## Contributions 🛠️

### [OpenBSD](https://www.openbsd.org/) 🐡

* **LDP: fixed adjacency processing logic**
    * Modified the adjacency lookup logic to include both source IP and LSR ID, preventing stale neighbor entries when the LSR ID is changed on the remote peer.
    * 🌐 [View Patch in openbsd-tech mailing list](https://marc.info/?l=openbsd-tech&m=156891357329836)
    * ⚙️ [View Commit in OpenBSD source](https://github.com/openbsd/src/commit/ddc8fec13db25891d49e4fa3a85e9844014a17eb)

### [Wireshark](https://www.wireshark.org/) 🦈

* **BGP: fixed dissector checks for labeled prefix parsing**
    * Corrected BGP prefix length validation for SAFI 4, 128, 129, and 130 to resolve default route display issues, integrating it with RD-aware checks.
    * ⚙️ [View Commit in Wireshark](https://gitlab.com/wireshark/wireshark/-/commit/133153238795ceaa18ae73786cd538dc9e2b5b12)
    * ⚙️ [View Commit in Wireshark mirror](https://github.com/wireshark/wireshark/commit/133153238795ceaa18ae73786cd538dc9e2b5b12)

## Research & Technical Proposals 🔍

### [Linux](https://kernel.org/) 🐧
* **FIB: fixed fib_info hash collisions for IPv4 routes with MPLS labels**
    * Identified a performance bottleneck in `fib_info_hash` where O(N) lookup complexity caused significant delays during large-scale MPLS route updates.
    * Proposed a `.get_encap_hash` callback for `lwtunnel_encap_ops` to include MPLS label sets in `fib_info` hash calculations.
    * Technical Outcome: Achieved a 400x speedup (from 6m to 0.8s for 100k routes); technical discussion confirmed the issue and established Nexthop API as the preferred architectural alternative.
    * 🌐 [View Technical Discussion in netdev mailing list](https://lore.kernel.org/netdev/20260222010820.8994-1-guschin108@gmail.com/t/#u)



