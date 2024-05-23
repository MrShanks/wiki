# OSI-Model

In plain English, the OSI provides a standard for different computer systems to be able to communicate with each other.

The OSI Model can be seen as a universal language for computer networking. It is based on the concept of splitting up a communication system into seven abstract layers, each one stacked upon the last.

| Layer | Description | Protocols/Purpose |
|-------|-------------|-----------|
| Application Layer | Human-Computer interaction layer, where applications can access the network servicesa | HTTP SMTP |
| Presentation Layer | Ensure that data is in a usable format and is where data encryption occurs | Encryption and Compression of data |
| Session Layer | Maintains connections and is responsible for controlling ports and sessions | Opens and close communication between the two talking devices |
| Transport Layer | Transmits data using transmission protocols | TCP/UDP Responsible for end to end communication and chunking the message into packets to be sent on layer 3 |
| Network Layer | Decides which Physical path the data will take | ICMP Helps routing packages to the right device on the same network there is no need for layer 3 |
| Data Link Layer | Defines the format of data on the network | Handles Hop to Hop communication on the same network using MAC Addresses |
| Physical Layer | Transmits raw bit stream over the physical medium | Cables and switches, data is converted into a bit stream |