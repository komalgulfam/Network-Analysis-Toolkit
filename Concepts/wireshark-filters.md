# Wireshark Display Filters Reference

| Requirement | Display Filter |
| :--- | :--- |
| HTTP Requests (GET Method) | `http.request.method == "GET"` |
| HTTP Domain Match | `http.host contains "example.com"` |
| HTTPS Domain Match (YouTube/Google) | `tls.handshake.extensions_server_name contains "youtube"` |
| DNS Request Match | `dns.qry.name contains "youtube"` |
| Source IP Filter | `ip.src == IP_ADDRESS` |
| Destination IP Filter | `ip.dst == IP_ADDRESS` |
