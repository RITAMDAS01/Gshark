Gshark | Neural Forensics

Gshark is a purely browser-based, AI-augmented network packet analysis tool. It parses raw PCAP and PCAPNG capture files locally and leverages Google's Gemini Large Language Models (LLMs) to perform deep heuristic audits on network frames.

⚠️ The Architecture: Why Client-Side?

Network forensics tools are notoriously memory-intensive. Uploading 100MB+ PCAP files to a server-side backend (like a free-tier Flask/Render instance) will inevitably result in Out-Of-Memory (OOM) crashes.

Gshark solves this by bypassing the server entirely.

Local Parsing: 100% of the binary packet dissection (PCAP & PCAPNG) happens in the user's browser using JavaScript DataView. Zero server RAM is consumed.

Direct AI Link: The application connects directly to the Google Gemini API from the client.

✨ Features

Universal Capture Support: Dynamically detects and parses both classic PCAP and modern PCAPNG binary formats, including support for Large Receive Offload (LRO) frames and 802.1Q VLAN tags.

Neural Querying: Filter traffic using natural language (e.g., "Show me only DNS traffic"). The AI translates this into strict application filters.

Deep Heuristic Audit: Select any frame and send its hex dump to the AI. Gshark extracts a tactical JSON report detailing:

Traffic Signature Classification

Threat Level (SAFE to CRITICAL)

Detected Anomalies

Tactical Directives for Investigators

Topology Mapping: Automatically maps unique endpoint communications and flags potentially risky nodes based on primitive protocol heuristics.

Zero-Install: It's a single HTML file. No npm install, no backend configurations, no Docker containers.

🚀 Getting Started

Prerequisites

You need a Google Gemini API Key. You can get one for free from Google AI Studio.

Installation & Execution

Clone this repository or download the gshark.html file.

Double-click gshark.html to open it in any modern web browser (Chrome, Edge, Firefox, Brave).

Navigate to the Configuration tab (the gear icon).

Paste your Gemini API Key into the vault. (Note: This key is stored securely in your browser's local localStorage and is never sent anywhere except directly to Google's API).

Click Ingest to upload your .pcap or .pcapng file.

🛠️ Tech Stack

Frontend: React 18 (via standalone CDN)

Styling: Tailwind CSS (via CDN)

Transpilation: Babel (in-browser)

AI Integration: Google Generative Language API (gemini-2.5-flash)

🔒 Security & Privacy Notice

Because this is a static, client-side application:

Your PCAP files never leave your computer. They are read entirely in the browser's memory.

Only the specific frames you choose to "Audit" are sent to the AI. Do not audit frames containing highly sensitive, unencrypted PII or credentials, as that specific payload text is sent to Google's API for analysis.

License

This project is licensed under the MIT License - see the LICENSE file for details.
