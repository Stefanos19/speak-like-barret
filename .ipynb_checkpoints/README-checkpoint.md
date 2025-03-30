# 🧠 Speak Like a FFVII Character

This is an exploratory and educational repository that finetunes a pre-trained GPT-2 model using dialogue from a specific character in *Final Fantasy VII* by Square Enix. The goal is to make the model emulate the unique speaking style of that character.

---

## 📚 Inspired By

This project is based on two excellent tutorials:

- 🎥 [Let's Reproduce GPT-2 (124M)](https://www.youtube.com/watch?v=l8pRSuU81PU) by Andrej Karpathy ([Source Code](https://github.com/karpathy/build-nanogpt))
- 🎥 [LoRA: Low-Rank Adaptation of Large Language Models - Explained Visually + PyTorch Code](https://www.youtube.com/watch?v=PXWYUTMt-AU&t=1385s) by Umar Jamil

---

## 🚀 Getting Started

### 1. Extract Character Dialogue

First, we can find the **FFVII dialog script** from the [Final Fantasy wiki](https://finalfantasy.fandom.com/wiki/Final_Fantasy_VII_script). I have saved it as:

```
data/dialog.html
```

Then open `text_extract.ipynb` and specify in the first line the character whose dialogue you want to extract. For example:

```
character = "Barret"
```

This notebook will:

- Parse the HTML file  
- Extract only the dialogue lines for the chosen character  
- Save the lines to `data/train.txt`

---

### 2. Finetune the GPT-2 Model

You now have two options to finetune the model:

#### Option 1: Full Finetuning

Run the notebook:

```
finetune_full.ipynb
```

#### Option 2: LoRA Finetuning

Run the notebook:

```
finetune_lora.ipynb
```

Both notebooks use the same pre-trained GPT-2 model file (`model_gpt2.pt`), trained following Karpathy's tutorial.

📥 Download the pre-trained model here:  
[Download gpt2_model.pt](https://www.dropbox.com/scl/fi/dzn6q4d3pxsqpqkm227of/gpt2_model.pt?rlkey=1d0d61ab0vwknlrrqqb64ncfz&st=mx0b6lpy&dl=0)

---

## ⚠️ Limitations

Due to the small size of the script data, the model can **mimic the character’s style**, but **maintaining coherence** over longer outputs remains a challenge without overfitting.

---

## 💡 Feedback & Contributions

Suggestions for improvement are very welcome!  
Reach out to me on [Twitter](https://twitter.com/Stefanos19)

