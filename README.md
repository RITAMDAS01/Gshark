⚡ Gshark

Browser-native packet analysis. Zero backend. Zero nonsense.

Gshark is a fully client-side network forensics tool that parses .pcap and .pcapng files directly in your browser — no uploads, no servers, no waiting around for some cloud instance to choke and die.

It pairs local packet dissection with Google Gemini AI to give you intelligent, on-demand analysis of your traffic.

🚀 Why This Exists

Most packet analysis tools assume:

You’re okay uploading sensitive traffic to a server
You have unlimited memory
Or you enjoy watching cloud services crash

Gshark does the opposite:

Everything runs locally
Your data stays on your machine
AI analysis happens only when you explicitly ask for it
🧠 Core Features
🔍 Universal PCAP Parsing
Supports both PCAP and PCAPNG
Handles:
LRO (Large Receive Offload)
VLAN tagging (802.1Q)
Built using efficient DataView parsing in JavaScript
💬 Natural Language Filtering

Skip writing filters like it’s 2005.

Just type:

“Show DNS traffic from 192.168.1.0/24”

And get results instantly.

🧬 AI-Powered Packet Analysis

Click any frame → get a structured JSON report with:

Traffic classification
Threat assessment
Anomaly detection
Payload breakdown
Suggested next actions

No guesswork. Just answers.

🌐 Network Topology Mapping

Automatically maps communication between endpoints into a visual graph.

Because staring at raw packets forever is not a personality.

📦 Zero-Install Architecture
Single HTML file
No dependencies
No backend
No Docker rabbit hole

Just open and go.

🏗️ How It Works
Local-First Processing

All parsing happens inside your browser memory.
Your PCAP files never leave your machine.

Direct AI Integration

When you request analysis:

Only the relevant hex dump is sent
Data goes directly to Google Gemini API
No intermediate servers involved
🛠️ Getting Started
Get a Gemini API Key
Head to Google AI Studio and grab one.
Download the App
Open gshark.html in a modern browser.
Configure
Paste your API key into the settings panel
Analyze
Upload your .pcap or .pcapng
Start digging
🔐 Security & Privacy
✅ PCAP files stay local
✅ No background uploads
✅ Only selected packet data is sent for AI analysis
❌ No hidden server-side processing

If something leaves your machine, it’s because you told it to.

📜 License

MIT License.
Do whatever you want, just don’t pretend you wrote it.
