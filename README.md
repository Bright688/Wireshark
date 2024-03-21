# Wireshark
to convert pcap to csv use tshark command in terminal:

tshark -r input.pcap -T fields -E separator=, -E quote=d -E occurrence=a -e frame.number -e frame.time -e ip.src -e ip.dst -e tcp.srcport -e tcp.dstport -e udp.srcport -e udp.dstport -e icmp.type -e icmp.code -e dns.qry.name -e dns.resp.name -e http.request.method -e http.request.uri -e http.response.code -e http.user_agent -E header=y > output.csv
