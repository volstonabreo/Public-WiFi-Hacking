
# Public WiFi Hacking

<br><br>
<p align="center">
  <a href="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Public%20WiFi%20Hacking.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1h2twrBb6UFNGRPrBiIgxzS_S9tUTfHqW%26export%3Ddownload">
    <img src="/img/WiFiHacking.svg">
  </a>
</p>
<br>

## The Attack

A victim machine connects to an official access point with the SSID “Caribou Coffee Guest”. An attacker enters with a Raspberry Pi and network adaptor, sets up a fake access point with the same SSID “Caribou Coffee Guest” and channel. The fake access points has a DHCP service running and an iptables rule for NATing outgoing traffic.

The attacker then launches a de-authorization attack where he actively sends deauthorization packets to both the official access point and the victim machine to disconnect the original connection, while the fake access point is broadcasting a signal that is higher than the official access point, effectively disconnecting the victim machine from the official access point and automatically connecting to the fake access point.

Now that the victim machine is connected to the fake access point, the attacker spoofs the DNS to redirect the victim machine to a phishing page to steal credentials.
