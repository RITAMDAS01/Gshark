The software application herein designated as Gshark is engineered to execute the parsing of raw PCAP and PCAPNG capture files exclusively within the confines of a localized web browser environment. Furthermore, it utilizes the Gemini Large Language Models provided by Google to conduct comprehensive heuristic audits upon network frames. Consequently, the requisite for any server-side processing infrastructure is entirely obviated.

Principal Functional Specifications

Universal Binary Parsing Mechanics: The system is designed to dynamically identify and process both the legacy PCAP and the contemporary PCAPNG file formats. The processing of Large Receive Offload (LRO) frames and 802.1Q Virtual Local Area Network (VLAN) tags is managed locally through the implementation of the JavaScript DataView interface.

Neural Querying Mechanisms: Packet captures may be filtered via natural language inputs; for instance, queries may be formulated to isolate Domain Name System traffic originating exclusively from a specified local subnet.

Comprehensive Heuristic Auditing: Upon the deliberate selection of any given frame, a structured JSON report is generated and extracted, which enumerates the following analytical parameters:

Traffic Signature Classification

Threat Level Assessment

Detection of Anomalies

Payload Decomposition and Subsequent Tactical Directives

Topology Mapping: The unique communications established between endpoints are mapped autonomously to facilitate the visual representation of the network graph.

Zero-Installation Infrastructure: The application is encapsulated entirely within a singular HTML document, thereby negating the requirement for package managers, backend dependencies, or containerization protocols.

Architectural Framework

Tools designed for network forensics are generally recognized to require substantial memory allocations. The transmission of voluminous PCAP files to server-side backends—particularly those hosted on gratuitous cloud tiers—frequently precipitates Out-Of-Memory (OOM) structural failures.

Gshark is purported to resolve such limitations through the complete circumvention of backend infrastructure.

Localized Dissection: The entirety of the binary packet dissection processes is executed strictly within the memory constraints of the localized web browser.

Direct Artificial Intelligence Linkage: The application establishes a direct connection to the Google Gemini Application Programming Interface (API) directly from the client device.

Procedural Initialization Instructions

To initialize the application, the requisite components are limited to a compatible web browser and a valid API key.

Acquisition of the API Key: A Gemini API Key must be obtained via the Google AI Studio portal.

Application Launch: The gshark.html file must be downloaded from the respective repository and subsequently executed within a contemporary web browser environment.

Vault Configuration: The operator is required to navigate to the configuration interface wherein the obtained Gemini API Key must be securely inserted.

Execution of Analysis: The designated ingest function must be selected to facilitate the upload of the requisite .pcap or .pcapng file, thereby commencing the investigative protocol.

Security and Privacy Protocols

Given that the program is constituted as a static, client-side application, the following operational conditions are asserted:

Data Retention: The capture files are retained locally; the binary parsing engine operates strictly within the localized browser memory, ensuring that said files are never transmitted to external servers.

Selective Data Transmission: It is strictly the specified hexadecimal dump of a frame—expressly designated for auditing or neural querying purposes—that is transmitted to the Google API for analytical processing.

Licensing Declaration

This software project is distributed under the terms of the MIT License. Reference to the appended LICENSE document is advised for comprehensive details regarding permitted utilization and legal restrictions.
