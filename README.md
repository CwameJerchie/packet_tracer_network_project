# packet_tracer_network_project
This project simulates a company network infrastructure that features internal client communication, domain name resolution, public web hosting, and secure external access via static routing and Network Address Translation (NAT). Implemented and tested using Cisco Packet Tracer.

# Company Network Simulation (Cisco Packet Tracer)

This project simulates a company’s internal and external network using Cisco Packet Tracer. It includes NAT, DNS, static routing, and HTTP hosting, demonstrating both internal and external client access to a public-facing web server.

## 📦 Features

- ✅ Two internal client PCs (PC0, PC1)
- 🌐 Web Server hosting www.company.com
- 📡 DNS Server resolving domain to IP
- 🔁 Static routing between routers
- 🔄 Static NAT to expose web server to external clients
- 🧭 ExtPC simulating an external user

## 🖥 Network Topology


[PC0, PC1] -- Switch -- R1 -- ISPRt -- ExtPC
                      |
                    WebSrv (192.168.1.50)
                    DNS1   (192.168.1.60)


- *R1*
  - LAN: 192.168.1.1/24 (FastEthernet0/0)
  - WAN: 10.0.0.1/24 (FastEthernet1/0)
- *ISPRt*
  - R1 side: 10.0.0.254/24 (FastEthernet0/0)
  - ExtPC side: 10.0.1.1/24 (FastEthernet0/1)
- *ExtPC*
  - IP: 10.0.1.10/24
  - Gateway: 10.0.1.1
  - DNS: 192.168.1.60

## 🌐 DNS Record

| Domain           | IP Address    |
|------------------|---------------|
| www.company.com  | 10.0.0.1      |

## 🔁 NAT Configuration

On *R1*:
bash
ip nat inside source static 192.168.1.50 10.0.0.1


## 🧪 How to Run

1. Open the .pkt file in Cisco Packet Tracer
2. Use a browser on:
   - PC0 or PC1 → http://www.company.com
   - ExtPC → http://www.company.com
3. Test DNS and ping paths using CLI on all PCs

## 📂 Included Files

- DNS_WebSrv_Configure.pkt - the full Packet Tracer file

---

Created for networking practice and simulation purposes. Enjoy!
"""
I have attached the following PNG files below for clarity and a step-by-step process

![R1NatConfigure](https://github.com/user-attachments/assets/c3f4f49f-6ff6-4614-a6db-5f84b72795ea)
![R1FE10](https://github.com/user-attachments/assets/8f58ec0d-64ce-4d19-8e20-e3727c4ada16)
![R1FE00](https://github.com/user-attachments/assets/50a933e6-ef2f-442e-9532-55f2f15b72a2)
![PC1Configure](https://github.com/user-attachments/assets/b856e3c0-6b43-4876-b3fb-5ef43780bd02)
![PC0Configure](https://github.com/user-attachments/assets/634d59d0-1ebe-4f9f-b6d8-3a13f638d13b)
![Initialsetup](https://github.com/user-attachments/assets/e82ab4f5-d437-4107-8f07-5600dc168ea4)
![html](https://github.com/user-attachments/assets/a655fb50-b4b6-491b-a0f4-ba5ffee6b798)
![finalview](https://github.com/user-attachments/assets/12ea059d-7e91-4494-b3bd-94281dc76e2f)
![ExtPCconfigure](https://github.com/user-attachments/assets/116d664a-b5bb-43d1-9e7c-c3f12b169cd3)
![ExtPCBrowse](https://github.com/user-attachments/assets/7e9fb21d-19d5-4a3b-9769-808f4f0474bb)
![DNS1FEConfigure](https://github.com/user-attachments/assets/e276b96f-c2f5-4a9d-97aa-3bfa716eaefc)
![DNS1configure](https://github.com/user-attachments/assets/26d7b955-2e80-4c58-9d9e-ad01336c6933)
![Arecord10001](https://github.com/user-attachments/assets/b7ca2f10-6d04-4a29-a627-53dbc7d3a69d)
![WebSrvConfigure](https://github.com/user-attachments/assets/94201c5d-92f6-47c7-b9d4-220fcb12895e)

