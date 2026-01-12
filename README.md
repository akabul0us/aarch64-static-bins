## aarch64_linux static-PIE binaries

This repo contains:
- [Aircrack-ng suite](https://www.aircrack-ng.org/) v1.7
- [BusyBox](https://www.busybox.net) v1.37.0 [^1] 
- [Dropbear](https://matt.ucc.asn.au/dropbear/dropbear.html) v2025.88 [^2]
- [Hashcat](https://hashcat.net/hashcat/) v7.1.2
- [Ethtool](https://git.kernel.org/pub/scm/network/ethtool/ethtool.git) v6.14.2
- [mdk4](https://github.com/aircrack-ng/mdk4) v4.2
- [nmap](https://www.nmap.org) v7.98 [^3]
- [socat](http://www.dest-unreach.org/socat/) v1.8.0.3 [^4]
- [strace](https://strace.io) v6.17 [^5] 
- [toybox](https://www.landley.net/toybox/) v0.8.13
- [zsh](https://www.zsh.org/) v5.9

The toolchain I used to build these is available [here](https://github.com/akabul0us/musl_linux_static_toolchains)

[^1]: for full list of applets, check [INSTALL.sh](INSTALL.sh).
[^2]: compiled as multi-call binary `dropbearmulti` with all programs enabled - `ssh`/`dbclient`, `scp`, `dropbear`, `dropbearconvert`, `dropbearkey`/`ssh-keygen` 
[^3]: compiled with: `nmap-liblua-5.4.8 openssl-3.5.2 nmap-libssh2-1.11.1 libz-1.3.1 libpcre2-10.46 nmap-libpcap-(with nmap-libdnet-1.18.0 ipv6`
[^4]: compiled with: `help`, `stats`, `stdio`, `fdnum`, `file`, `creat`, `gopen`, `termios`, `pipe`, `socketpair`, `unix`, `abstract_unixsocket`, `ip4`, `ip6`, `rawip`, `genericsocket`, `interface`, `tcp`, `udp`, `sctp`, `dccp`, `udplite`, `listen`, `posixmq`, `socks4`, `socks4a`, `socks5`, `vsock`, `namespaces`, `proxy`, `system`, `shell`, `exec`, `sycls`, `filan`, `retry`, `tun`, `pty`, `openssl` // without: `fips`, `libwrap`, `devtests`, `readline` // `msglevel=0` // `default_ipv=4`
[^5]: compiled with: `m32-mpers`
