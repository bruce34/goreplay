# Building

git clone https://github.com/bruce34/goreplay.git
cd goreplay
git checkout t-master
sudo make  build && sudo make release-bin
mv gor goreplay
fpm -s dir -t rpm  -n goreplay -v 0.16.1_110 --description "goreplay 0.16.1 100 continue fixes, configurable RX buffer, http-set-header fix, immediate-mode, large pcap buffers, coalesce packets, large snaplen, chunked transfer fixes. Built from https://github.com/bruce34/goreplay.git t-master" --prefix /usr/local/bin goreplay

