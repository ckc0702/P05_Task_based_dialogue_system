# P05_Task_based_dialogue_system

The aims of this project is to develop a task-based dialogue system capable of doing intent detection and slot filling task which are important problem for virtual assistant system. The proposed system for this project consist of three main components: Shared Encoder, Cross Attention Module, and Decoder. 

1. Shared Encoder
- Pre-trained BERT (transfer learning - word embedding)
- Convolutional Layer (focus local semantics between words)
- BiLSTM Layer (focus global semantics between words)

2. Co-Interactive Module
- by Qin et al., 2020, A Co-Interactive Transformer for Joint Slot Filling and Intent Detection
- Facilitate Joint-learning, which join the computation of loss of intent detection and slot filling task to improve model performance as both of these tasks are dependent to each other

3. Decoder
- Two classifier: intent decoder and slot decoder
- Intent decoder to obtain sentence representation to compute accuracy of intent detected from sentence 
- Slot decoder applied conditional random field algorithm to compute the negative log likelihood for the slot tags

Benchmark:
1. Intent detection uses accuracy metric
2. Slot filling uses F1 score metric
3. Overall accuracy (sent - sample with all intent and slot filling tags correctly predicted) uses accuracy metric
   
![image](https://github.com/ckc0702/P05_Task_based_dialogue_system/assets/59757087/1af33938-dfb9-4f02-87ec-ece2624dc920)
