# p-captivate

Multicast PCAP Analyzer — single‑file Flask app


Features
- Upload a .pcap/.pcapng and analyze for multicast health signals
- No tshark dependency; uses scapy for parsing
- Detects IGMP activity (queries/reports/leaves) and multicast groups
- Summarizes multicast UDP streams by group: bitrate, pps, jitter
- Optional RTP loss/sequence analysis when RTP v2 is detected
- Flags noisy discovery (mDNS/SSDP) and TTL pitfalls
- Shows VLAN tags (802.1Q) observed on multicast packets


Usage
pip install -r requirements.txt # see REQUIREMENTS string below
python app.py
# then open http://127.0.0.1:5000


Security note: This demo keeps uploads in /tmp and deletes after parse.
Adjust MAX_CONTENT_LENGTH as needed.
"""
