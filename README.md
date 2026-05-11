# AQUA - AI Voice Store 🛒

AQUA is an advanced, AI-powered e-commerce voice assistant designed to provide a seamless shopping experience. It combines conversational AI with a visual product catalog, allowing users to browse items, add them to their cart via voice, and interact with the store using both speech and visual cues.

## 🚀 Features

* **Conversational Shopping**: Interact with the "AQUA Assistant" using natural voice commands to find products and manage your cart.
* **Visual Product Catalog**: A dynamic frontend that displays products with images, names, and prices directly from the store's inventory.
* **Voice-to-Cart Logic**: Add products to your shopping cart simply by speaking (e.g., "Add two milk packets to my cart").
* **AI-Powered Reasoning**: Utilizes **Google Gemini 2.0 Flash** to understand user intent, handle product queries, and provide intelligent shopping recommendations.
* **Speech-to-Text & Text-to-Speech**: Integrated with **AssemblyAI** for high-accuracy transcription and **Murf AI** for professional, friendly voice responses.
* **Visual Search Integration**: Prepared for the future of shopping with a dedicated visual search interface (Camera UI) for image-based product discovery.
* **Order Management**: Automatically calculates totals and saves finalized orders to a local `orders.json` file for persistence.

## 🛠️ Tech Stack

### Backend

* **Framework**: FastAPI.
* **AI Models**: Google Gemini 2.0 Flash (Reasoning).
* **Transcription**: AssemblyAI (STT).
* **Voice Synthesis**: Murf AI (TTS).
* **Environment**: Python-dotenv.

### Frontend

* **Styling**: Tailwind CSS with a clean, modern e-commerce aesthetic.
* **Interactions**: Vanilla JavaScript with Axios for real-time state management.
* **Assets**: Local product image hosting.

## 📂 Project Structure

```text
├── backend/
│   ├── main.py              # FastAPI server and CORS configuration
│   ├── routes.py            # AI assistant logic and API endpoints
│   ├── commerce.py          # E-commerce utility functions
│   ├── grocery_catalog.json # Product inventory database
│   ├── orders.json          # Historical order records
│   └── requirement.txt      # Backend dependencies
├── frontend/
│   ├── index.html           # Main store UI with catalog and cart
│   ├── index.js             # Voice processing and UI update logic
│   └── products/            # Static product image assets
└── .env                     # API keys for Google, AssemblyAI, and Murf

```

## ⚙️ Setup & Installation

### Backend Setup

1. Navigate to the `backend` directory.
2. Install the required Python packages:
```bash
pip install -r requirement.txt

```


3. Create a `.env` file and add your API credentials:
```text
GOOGLE_API_KEY=your_gemini_key
ASSEMBLYAI_API_KEY=your_assemblyai_key
MURF_AI_API_KEY=your_murf_key

```


4. Start the server:
```bash
python main.py

```



### Frontend Setup

1. Navigate to the `frontend` directory.
2. Install dependencies:
```bash
npm install

```


3. Launch `index.html` via a local development server (like VS Code Live Server).

## 📖 How to Use

1. **Enter Store**: Click "ENTER STORE" to initialize the voice assistant and receive a welcoming greeting.
2. **Browse & Speak**: Use the microphone button to ask for items or specify quantities to add to your cart.
3. **Visual Catalog**: Click on product images to view details or use the camera icon to simulate a visual search.
4. **Manage Cart**: Review your items and total bill in the "Your Cart" section, which updates in real-time based on your voice commands.
5. **Checkout**: Say "Place my order" or "I'm done" to finalize your purchase and save the order data.
