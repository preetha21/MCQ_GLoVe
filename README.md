T5-GloVe-Based Multiple-Choice Question Generation using SQuAD
This project demonstrates an end-to-end pipeline for automatic Multiple-Choice Question (MCQ) generation using pre-trained T5-base and GloVe embeddings, trained and evaluated on the SQuAD v1.1 dataset.

🔍 Core Features:
🧠 Question Generation: Fine-tuned t5-base model trained on context-answer pairs from SQuAD to generate high-quality, contextual questions.
💡 Distractor Generation: Uses GloVe word embeddings to identify semantically related but incorrect options as distractors.
🧹 Keyword Extraction: Optional RAKE-based keyword extraction used to enhance answer selection.
🧪 Evaluation-ready output: Generated questions are automatically structured as MCQs with one correct answer and 3 distractors.

⚙️ Techniques Used:
T5ForConditionalGeneration from Hugging Face Transformers
GloVe 300-d embeddings for distractor similarity matching
RAKE for keyword/answer phrase selection
SQuAD preprocessing and formatting pipeline
PyTorch-based training (Colab + CUDA support)

🚧 Limitations:
While effective for general-purpose MCQs, the use of static word vectors (GloVe) limits the contextuality of distractors, especially in technical or domain-specific texts.
This limitation is currently being addressed in a new version of the project that integrates Sentence-BERT for deeper semantic distractor generation and includes training on RACE + SciQ datasets.
