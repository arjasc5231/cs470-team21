# cs470-team21

project by 이중훈,한승우,박민규,이현석,김정원 in the course KAIST cs470 22fall

you can see the poster Team_21_poster_file.pdf

### dataset

download amazon review data : nijianmo.github.io/amazon/

in particular, we used ‘small Books 5-core.’

### preprocessing

run preprocess.ipynb to generate preprocessed dataset.

for evaluating, we labeled rationales and encoded using preprocess_rationale.ipynb. result : preprocessed_balanced_encoded.csv

### fine-tuining

we used pretrained BERT model and fine-tuned to follwing two models.

1. binary classification (positive or negative)
2. regression (rating)

run finetuing_binaryclassification.ipynb and finetuing_regression.ipynb

### generating explanation

using fine-tuned model, generate explanation for each review.

run generate_explanation_binaryclassification.ipynb and generate_explanation_regression.ipynb

you can choose XAI methods within transformer_attribution, partial_lrp, last_attn, attn_gradcam, lrp, rollout

### summarization

choose most important words Based on occurrences, ratings and generated scores.

run summarize_relevance_1129.ipynb

### visualization

visualize highlighted indivisual reviews and summary

run text_visualization_221129.ipynb

### evaluation

evaluate model based on IOU, AUPRC, comprehensiveness, sufficiency

run IOU_AUPRC.ipynb and comprehensiveness_sufficiency.ipynb
