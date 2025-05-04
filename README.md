# Image Classifier — Deep Learning Project

This project is an end-to-end **image classification pipeline** that classifies images using transfer learning with VGG16. It is built for production readiness with modular architecture, configuration management, callback handling, and structured evaluation.

---

## 🎯 Project Goals

- Build a binary image classifier using pre-trained models (transfer learning).
- Automate the ML workflow: data ingestion → preprocessing → training → evaluation.
- Apply **best practices** in code modularity, experiment tracking, and configuration-driven pipelines.

---

## 🧠 What’s Inside?

### ✅ Functional Modules
- **Data Ingestion**: Downloads dataset, unzips, and filters corrupted/empty files.
- **Base Model Preparation**: Loads and freezes VGG16 layers, adds custom classifier head.
- **Callbacks Setup**: Uses TensorBoard and ModelCheckpoint via dynamic timestamped directories.
- **Training Pipeline**: Fine-tunes the model with configurable hyperparameters.
- **Evaluation**: Loads trained model, performs validation, and logs metrics in `scores.json`.

---

## 🧰 Tech Stack & Tools

| Area           | Tools Used |
|----------------|------------|
| Language       | Python 3.8 |
| Framework      | TensorFlow, Keras |
| Model          | VGG16 (Transfer Learning) |
| Configuration  | YAML (`config.yaml`, `params.yaml`) |
| Visualization  | TensorBoard |
| Logging        | Python logging module |
| Packaging      | OOP classes and clean folder structure |
| OS Support     | Linux, macOS, Windows |

---

## 🗂️ Project Structure
```text
1. config.yaml            # Project structure, paths, URLs
2. params.yaml            # Hyperparameters (image size, LR, batch size)
3. Entity classes         # Map configs into typed Python objects
4. Configuration Manager  # Reads YAMLs, creates directories
5. Component modules      # Logic for data ingestion, callbacks, training, etc.
6. Pipeline scripts       # Orchestrate end-to-end flow
## 🗂️ Output
{
  "loss": 0.235,
  "accuracy": 0.927
}

