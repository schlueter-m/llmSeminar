# Chain-of-Thought (CoT) Prompting Experiments

## for the Seminar "Solving Complex Problems with Large Language Models" at Uni Mannheim

- dataset: [TAT-QA](https://nextplusplus.github.io/TAT-QA/)
	- test set comprises 100 questions 
- model: *gpt-3.5-turbo*
- design: comparing 3 prompt settings
	- Few-Shot (Manual) CoT prompting described in [this paper](https://proceedings.neurips.cc/paper_files/paper/2022/file/8bb0d291acd4acf06ef112099c16f326-Paper-Conference.pdf)
		- using 3 manually written exemplars (1 exemplar each for lookup >1, counting, calculating average task)
	- zero-shot CoT prompting described in [this paper](https://proceedings.neurips.cc/paper_files/paper/2022/file/9d5609613524ecf4f15af0f7b31abca4-Paper-Conference.pdf)
	- simple zero-shot prompting (Baseline)

![Prompt settings](https://github.com/schlueter-m//llmSeminar/blob/main/promptSettings.jpg?raw=true)

### Organization of repository: 
- `experiments.ipynb` contains selection and preparation of test set and model prompting
- `results_analysis.ipynb` contains analysis of model performances and error types
- `data/`
	- `tatqa_dataset` contains original data
	- `predictions/preds_answerFromTable_SETTING.xlsx` contain model answers for each prompt setting as well as labelled correctness and error types
	- `manual_cot_exemplars.xlsx` contains the three exemplars used in the few-shot CoT setting
	- `questions_overview_answerFromTable.xlsx` contains all metadata of the testset

