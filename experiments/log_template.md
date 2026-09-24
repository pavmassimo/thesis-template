# Experiment Log

Keep a record of every experiment here. This is your lab notebook—it should be detailed enough that someone else (or you, six months later) can understand what happened and why.

## Template Entry

**Date:** YYYY-MM-DD  
**Experiment ID:** exp_001  
**Objective:** What are we testing? (e.g., "Compare ResNet-8 vs MobileNetV2 on edge device")

**Environment:**
- Device: [e.g., Arduino, ESP32, mobile phone]
- OS/Framework: [e.g., TensorFlow Lite, PyTorch Mobile]
- Dependencies: [link to requirements.txt or conda.yml commit hash]

**Config:**
- Model: [architecture, pretrained or from scratch]
- Learning rate: 0.001
- Batch size: 32
- Epochs: 50
- Random seed: 42
- Data split: [train/val/test %, any stratification?]
- Preprocessing: [normalization, augmentation, etc.]

**Result:**
- Train accuracy: XX%
- Val accuracy: XX%
- Test accuracy: XX%
- Model size: XX MB
- Latency (inference): XX ms
- Energy consumption: XX mJ (if measured)

**Key Findings:**
- What worked well?
- What surprised you?
- What failed or was unexpected?

**Next Steps:**
- What would you try next?
- Any blockers?

**Notes:**
- Anything else? (e.g., "Training diverged after epoch 20—check data leakage", "Latency was much worse than expected; profile the model")

---

## Examples

### exp_001: Baseline MobileNetV2

**Date:** 2026-01-15  
**Objective:** Establish baseline performance on CIFAR-10 with MobileNetV2

**Environment:**
- Device: Raspberry Pi 4
- OS/Framework: TensorFlow Lite
- Dependencies: commit abc1234

**Config:**
- Model: MobileNetV2 (pretrained on ImageNet, fine-tuned on CIFAR-10)
- Learning rate: 0.001
- Batch size: 32
- Epochs: 50
- Random seed: 42
- Data split: 50k train, 10k val, 10k test
- Preprocessing: Normalization to [0, 1], no augmentation

**Result:**
- Train accuracy: 94.2%
- Val accuracy: 92.1%
- Test accuracy: 91.8%
- Model size: 12.2 MB
- Latency: 45 ms per inference
- Energy: Not measured

**Key Findings:**
- Model converged well; no signs of overfitting
- Latency is acceptable for real-time inference
- 12.2 MB fits comfortably in device memory

**Next Steps:**
- Try with data augmentation to see if we can push val accuracy higher
- Profile energy consumption on the Raspberry Pi

**Notes:**
- Validation accuracy plateaued around epoch 35; could try early stopping
- Baseline established; good reference point for next experiments
