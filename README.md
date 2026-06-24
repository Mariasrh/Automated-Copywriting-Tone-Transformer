# Automated Copywriting & Tone Transformer

This project is a dynamic orchestration engine designed to automate the generation of professional marketing copy[cite: 7, 16]. It leverages generative AI to transform raw product descriptions into platform-specific content (LinkedIn, Instagram, Email) by precisely tuning creative hyper-parameters like Temperature and Top_P[cite: 9, 16, 18, 20].

## Key Features
* **Dynamic Template Compilation:** Uses Python f-strings to inject user variables (`Product_Name`, `Platform`, `Tone`) into master instruction templates[cite: 9, 19, 87, 88].
* **Asynchronous Execution:** Utilizes `httpx` and `asyncio` to manage high-volume API requests efficiently, reducing total wall-clock time by overlapping network waiting periods[cite: 79, 121, 137, 139].
* **Parameter Control:** Programmatically adjusts model creativity and response length via `Temperature` and token limits (handling both legacy and modern reasoning models)[cite: 9, 20, 106, 111].
* **Scalable Pipeline:** Designed to build scalable content pipelines through pure inference logic, ensuring brand voice protection through structural prompt enforcement[cite: 10, 82, 91].

## Project Structure
* `main.py`: The core orchestration engine and asynchronous loop implementation[cite: 63, 145].
* `data.csv`: Input source for batch processing of metadata (Product, Target Tone, Platform Variables)[cite: 72].
* `requirements.txt`: Project dependencies including `httpx` for non-blocking I/O[cite: 154].
* `.gitignore`: Ensures secure handling of environment variables (like API keys) and temporary system files[cite: 80].

## How to Run

### 1. Prerequisites
Ensure you have Python 3.10+ installed.

### 2. Installation
Install the required asynchronous dependencies:
    ```bash
     pip install -r requirements.txt

### 3. Configuration
Set up your environment variables to securely store your API keys. 

> **Note:** Do not hardcode your keys directly into the script. Use a `.env` file instead.

### 4. Execution
Prepare your `data.csv` with the required columns (`Product_Name`, `Platform`, `Tone`) and run the orchestration engine:

```bash
python main.py
