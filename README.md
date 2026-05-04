# AI Credit Approval System

A professional, dual-model Artificial Intelligence system designed to evaluate credit risk and loan availability. This application leverages a hybrid architecture combining Foundation Models (TabPFN) and Gradient Boosting (CatBoost) to provide mathematically robust, highly accurate credit appraisals.

## Key Features

### Dual-Model Hybrid Architecture
- **Model 1 (German Credit):** Trained on the classic German Credit dataset, analyzing 20 complex financial data points to determine baseline credit reliability.
- **Model 2 (LaoTse Risk):** Trained on a massive modern Kaggle dataset, analyzing complex loan intents, interest rates, and employment spans to assess high-volume credit risk.
- **Ensemble Voting:** The backend dynamically balances predictions from both `TabPFN` (a transformer-based foundation model) and `CatBoost` to determine the final confidence score, virtually eliminating model-specific hallucinations.

### 🎨 Dynamic & Corporate UI Theming
- **AI Core Theme:** A modern, dark-mode glassmorphic aesthetic with animated floating gradients.
- **Bank Theme (MIYB):** A professional, flat, white-and-blue corporate theme designed for enterprise environments.
- **Dynamic Field Injection:** The UI instantly transforms its input form structure depending on which AI model is actively selected.

### 💱 Real-Time Purchasing Power Engine
Because historical datasets (like the 1994 German Credit set) use obsolete currencies and pre-inflation values, feeding them modern 2026 fiat currency breaks AI logic.
- **Live Exchange API:** The app continuously pulls live exchange rates using the `open.er-api.com` API.
- **Deflation Algorithm:** Converts the user's selected local currency (USD, EUR, GBP, TRY, etc.) into modern Euros, and mathematically deflates it back to **1994 Deutsche Marks (DM)** before secretly feeding it to the AI to ensure absolute historical accuracy.

## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/K4hveci/ai-credit-approval-system.git
   cd ai-credit-approval-system
   ```

2. **Configure Hugging Face Token:**
   The `TabPFN` foundation model requires a Hugging Face Token to download its internal checkpoint weights.
   - Create a file named `.env` in the root directory.
   - Add your token to the file:
     ```env
     HF_TOKEN=your_hugging_face_token_here
     ```

3. **Launch the System:**
   Simply double-click or run the included batch script:
   ```cmd
   .\start.bat
   ```
   *The script will automatically:*
   - Create a Python Virtual Environment.
   - Install required packages (PyTorch, TabPFN, CatBoost, Flask).
   - Start a local HTTP server for the Frontend on Port `8000`.
   - Start the Backend AI Engine on Port `5000`.
   - Open the web application automatically in your default browser.

---

### Credits
 **Made by:** Mehmet Efe Ergin, Yusuf Berk Baytok, Yunis Ibrahimov, Islam Pashazade