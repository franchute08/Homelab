# Pi-hole

Pi-hole is currently the main service running on my homelab. It provides DNS services for my local network and blocks ads and trackers at the network level.
## Purpose

I wanted to experiment with dns, learn more about ipv4 and also enjoy ad blocking at a network level.
## Setup

I installed the Pi-hole Docker image and created a container to run it on my server.
## Configuration

The server uses a static IPv4 address so that clients can consistently reach the DNS service.
After configuring the DNS settings in a device, I verified that client queries were reaching Pi-hole and that blocked requests were being detected in the dashboard.
## Troubleshooting

One of the main issues I encountered was related to the LAN's default DNS resolver configuration, wich was the router.
I had to disable the automatic DNS resolver and manually configure the DNS settings so that clients could use Pi-hole correctly.
## Testing

I tested Pi-hole by connecting clients to the server and monitoring DNS queries through the web dashboard.
While playing a mobile game I observed that with the automatic DNS resolver, ads were still being displayed, but after configuring the server as the DNS resolver. ads stopped showing up.
The queries were successfully reaching Pi-hole, and blocked requests were visible in the metrics, confirming that the service was working as expected.
