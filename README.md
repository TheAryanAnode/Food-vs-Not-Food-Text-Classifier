# Food vs Not-Food Text Classifier 🍔❌

This project fine-tunes a **DistilBERT-based text classification model** to determine whether a sentence is *literally about food* or *not about food*, even when food-related language is used metaphorically (e.g., “half-baked ideas”, “chewing on the problem”).

The model is trained using the Hugging Face ecosystem, evaluated for accuracy, benchmarked for inference speed, and deployed with an interactive **Gradio web interface**.

---

## 🚀 Features

- Fine-tuned **DistilBERT** for binary text classification
- Handles metaphorical and misleading food-related language
- Hugging Face `Trainer`-based training pipeline
- Accuracy evaluation and loss visualization
- Batch vs single-sentence inference benchmarking
- Deployed locally and via **Hugging Face Hub**
- Interactive **Gradio demo**

---

## 📂 Dataset

- **Source:** `mrdbourke/learn_hf_food_not_food_image_captions`
- **Classes:**
  - `food`
  - `not_food`
- Labels are mapped to numerical IDs for model training.

---

## 🧠 Model Details

- **Base model:** `distilbert-base-uncased`
- **Task:** Binary sequence classification
- **Frameworks:**
  - PyTorch
  - Hugging Face Transformers & Datasets
- **Training setup:**
  - Batch size: 32
  - Epochs: 10
  - Optimizer: AdamW (via Trainer)
  - Evaluation: Accuracy (per epoch)

---

## 📊 Training & Evaluation

- Tracks training and validation loss per epoch
- Automatically loads the best-performing model
- Final accuracy evaluated on a held-out test set
- Misclassifications and prediction confidence analyzed

Loss curves are visualized using Matplotlib to monitor overfitting and convergence.

---

## ⚡ Inference & Performance

Supports:
- Single-sentence inference
- Batch inference
- Hugging Face `pipeline`
- Direct PyTorch model calls

Inference speed is benchmarked across increasing batch sizes to demonstrate performance gains from batching.

---

## 🌐 Deployment

### Hugging Face Hub
The trained model is uploaded to the Hugging Face Hub for easy reuse:

