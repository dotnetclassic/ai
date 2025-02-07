## Communicating with Google Gemini 1.5 LLM

### Prerequisites
1. **Get API Key** from [Google AI Studio](https://ai.google.dev/)
2. **Install the Google AI SDK**:
   ```sh
   pip install google-generativeai
   ```

### Python Code to Communicate with Google Gemini 1.5

```python
import google.generativeai as genai

# Set up API Key (Replace with your own key)
API_KEY = "YOUR_GOOGLE_GEMINI_API_KEY"
genai.configure(api_key=API_KEY)

# Initialize the model
model = genai.GenerativeModel("gemini-pro")

def chat_with_gemini(prompt):
    response = model.generate_content(prompt)
    return response.text if response else "No response received."

# Example usage
if __name__ == "__main__":
    user_input = input("Enter your prompt: ")
    response = chat_with_gemini(user_input)
    print("\nGemini 1.5 Response:\n", response)
```

### Features
✅ Supports **Google Gemini-Pro (1.5)**  
✅ Can generate text-based responses  
✅ Uses Google AI SDK for interaction  

### Notes
- Replace `YOUR_GOOGLE_GEMINI_API_KEY` with your actual API key.
- If you need **multimodal support (text + image)** or **chat-based interaction**, let me know!