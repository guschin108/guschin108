# Vitaliy Guschin

System & Network Software Engineer focused on C/C++ development, networking protocols, and OS internals.

### 🛠 Contributions

#### [OpenBSD](https://www.openbsd.org/) 🐡
* **ldpd: Fixed adjacency processing logic**
  * Modified the adjacency lookup logic to include both source IP and LSR ID, preventing stale neighbor entries when the LSR ID is changed on the remote peer.
  * 🌐 [View Patch in openbsd-tech mailing list (2019)](https://marc.info/?l=openbsd-tech&m=156891357329836)
  * ⚙️ [View Commit in OpenBSD Source](https://github.com/openbsd/src/commit/ddc8fec13db25891d49e4fa3a85e9844014a17eb)

#### [Wireshark](https://www.wireshark.org/) 🦈
* **BGP: Fixed dissector checks for labeled prefix parsing**
  * Corrected BGP prefix length validation for SAFI 4, 128, 129, and 130 to resolve default route display issues, integrating it with RD-aware checks.
  * ⚙️ [View Commit in Wireshark Mirror](https://github.com/wireshark/wireshark/commit/133153238795ceaa18ae73786cd538dc9e2b5b12)
