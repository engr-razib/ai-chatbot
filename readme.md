Got it ✅ — here’s the **full markdown code** for your `README.md` file (you can copy-paste directly):

````markdown
# 🤖 HuggingFace.js Chatbot (Option 1 – Pure HTML)

This is a simple **browser-only chatbot** built with `huggingface.js` and the Hugging Face Inference API.  
No backend or extra frameworks required — just **one HTML file** you can open directly in your browser.

---

## 🚀 Features
- Uses [@huggingface/inference](https://www.npmjs.com/package/@huggingface/inference) (via [esm.sh](https://esm.sh/)) directly in the browser.
- Simple **chat UI** with streaming responses.
- No build tools or Node.js required — just open in a browser.
- Works with any Hugging Face **chat-capable model** (default: `mistralai/Mistral-7B-Instruct-v0.3`).

---

## 🛠 Setup Instructions

### 1. Get a Hugging Face API Token
1. Go to 👉 [Hugging Face Tokens](https://huggingface.co/settings/tokens).
2. Click **New token**.
3. Select:
   - **Type:** _Access token_
   - **Role:** _Read_
4. Copy the token (looks like `hf_xxxxx...`).

---

### 2. Save the HTML File
1. Copy the code from `chatbot.html` (provided in this repo).
2. Open the file and find this line:

   ```js
   const HF_TOKEN = "hf_your_token_here";
````

3. Replace it with your actual Hugging Face token:

   ```js
   const HF_TOKEN = "hf_abc123XYZ...";
   ```

---

### 3. Run Locally

You have two options:

#### 🔹 Option A: Open directly

* Double-click `chatbot.html`.
* It will open in Chrome/Edge/Firefox.
* Start chatting!

#### 🔹 Option B: Serve with a local server (recommended if imports fail)

Some browsers block `import` statements in local files. If that happens:

1. Install a simple server (requires Node.js):

   ```bash
   npm install -g serve
   ```
2. Start the server in the folder where `chatbot.html` is saved:

   ```bash
   serve .
   ```
3. Open [http://localhost:3000/chatbot.html](http://localhost:3000/chatbot.html) in your browser.

---

## 🧪 Usage

* Type your message in the input box.
* Press **Enter** or click **Send**.
* The chatbot will stream tokens from Hugging Face until the reply finishes.

---

## ⚠️ Security Warning

This demo **puts your Hugging Face token in the browser**.
That means anyone who sees the HTML source can also see your token.

✅ Fine for **local experiments**.
❌ Not safe for **public deployment**.

If you want to make this public, use a **proxy server** (see Option 2 in the guide).

---

## 🔧 Changing Models

By default it uses:

```js
const MODEL = "mistralai/Mistral-7B-Instruct-v0.3";
```

You can switch to any supported chat model on Hugging Face (e.g. `HuggingFaceH4/zephyr-7b-beta`).

---

## 📸 Preview

*(Screenshot of chatbot UI — dark theme with streaming responses)*

---

## 📚 References

* [Hugging Face Inference API Docs](https://huggingface.co/docs/api-inference/detailed_parameters)
* [huggingface.js](https://github.com/huggingface/huggingface.js)

---

## ✅ License

MIT – use freely for experiments and learning.

```
