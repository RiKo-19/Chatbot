# Chatbot

# 🗨️ Local CLI Chatbot using Flan-T5  

This project is a **command-line chatbot** built as part of the ATG Technical Assignment.  
It uses **Hugging Face’s Flan-T5 model** for text generation, with a **sliding window memory** and a **fallback mechanism** to ensure more accurate answers for common factual questions.  

---

## 📌 Features
- ✅ Uses **Flan-T5-base** (`google/flan-t5-base`) as the main text generation model.  
- ✅ Maintains **short-term memory** (last 3–5 turns) for context.  
- ✅ Expands follow-up queries (*“And India?”*) into full questions (*“What is the capital of India?”*).  
- ✅ **Fallback validator** ensures correct answers for common factual queries (e.g., capitals).  
- ✅ Simple **CLI interface** with `/exit` command to quit.  
- ✅ Modular structure with separate files:
  - `model_loader.py` → Loads Hugging Face model  
  - `chat_memory.py` → Sliding window memory  
  - `interface.py` → CLI loop + integration + fallback logic  

---

## 🛠️ Setup

1. **Clone or download** the repository.  

2. Install dependencies:
   ```bash
   pip install transformers
   ```

3. Run the chatbot:
   ```bash
   python interface.py
   ```

---

## 💻 Usage Example
```
Flan-T5 Chatbot started. Type /exit to quit.

User: Hi
Bot: Hello! How are you doing?

User: What is the capital of France?
Bot: The capital of France is Paris.

User: And Italy?
Bot: The capital of Italy is Rome.

User: And India?
Bot: The capital of India is New Delhi.

User: Tell me a joke
Bot: Why don’t scientists trust atoms? Because they make up everything!

User: Who are you?
Bot: I am a chatbot powered by Flan-T5.

User: /exit
Exiting chatbot. Goodbye!
```

---

## 📂 Project Structure
```
chatbot/
│── model_loader.py   # Loads Flan-T5 model
│── chat_memory.py    # Sliding window memory buffer
│── interface.py      # CLI chatbot with fallback + query expansion
│── README.md         # Documentation
```

---

## 🎥 Demo Video
- Record a short **2–3 min video** showing:
  - Folder structure  
  - Code explanation (model loader, memory, interface)  
  - Running chatbot in terminal  
  - Few example Q&A interactions  
- Upload to **Google Drive or YouTube (unlisted link)**  

---

## 📌 Notes
- This chatbot is **not a perfect knowledge model** — Flan-T5 is an instruction model and may hallucinate.  
- The **fallback system** ensures factual accuracy for certain queries (e.g., capitals, jokes, identity).  
- The focus of this assignment is **integration, memory handling, and CLI interface**.  

---

## 📊 Deliverables
- ✅ Modular Python scripts  
- ✅ README.md with setup & examples  
- ✅ Demo video link  
- (Optional) Jupyter notebook if prototyped  

---

✨ That’s it — your CLI chatbot with Flan-T5 is ready!  
