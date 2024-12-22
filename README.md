# Protocol Network Platform

A modular, high-performance network protocol analysis platform providing core protocols, extensible protocol packs, blockchain support, and real-time intelligence capabilities.

## Overview

The Protocol Network Platform consists of several SDKs that work together to provide comprehensive network protocol analysis and processing capabilities:

- **jnetpcap-sdk**: High performance native packet capture
- **protocol-sdk**: Extensible protocol analysis framework
- **blockchain-sdk**: Blockchain protocol support 
- **intelligence-sdk**: Real-time network analytics

## Key Features

- High performance packet processing engine
- Extensive protocol support through modular protocol packs
- Real-time protocol analysis and intelligence
- Blockchain protocol analysis capabilities
- Flexible pipeline architecture 
- Protocol-aware analytics
- Extensible architecture

## Architecture

The platform uses a modular design with clean separation between:

- Packet capture and processing (jnetpcap)
- Protocol analysis framework (protocol-api)
- Protocol implementations (protocol packs)
- Intelligence/analytics capabilities

This allows for independent versioning, licensing and deployment of components.

## Quick Start

```java
// Initialize capture  
try (NetPcap pcap = NetPcap.live()) {
    
    // Configure protocol processing
    pcap.setPacketFormatter(new PacketFormat());
    pcap.activate();
    
    // Process packets
    pcap.loop(100, (String user, Packet packet) -> {
        // Access protocol headers
        if (packet.hasHeader(ip4)) {
            System.out.println(ip4);
        }
    });
}
```

## Documentation

- [Protocol API Reference](docs/protocol-api.md)
- [Protocol Pack Guide](docs/protocol-packs.md)
- [Analytics Reference](docs/analytics.md) 
- [Examples](examples/)

## License

The core platform (protocol-api) is available under the Apache 2.0 license.
Individual protocol packs and analytics modules are available under commercial license.

Contact Sly Technologies for licensing details.

## Support

- [Documentation](https://www.slytechs.com/docs)
- [Commercial Support](https://www.slytechs.com/support)
- [Training](https://www.slytechs.com/training)
