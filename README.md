#AutoOracle_Dataset

Introduction:

This dataset is the first large-scale, high-quality C++ Test-Assert Pair (TAP) dataset proposed and constructed by Samsung Electronics, designed to support research on automated test oracle generation using large language models (LLMs). This data was built from 666 open-source C++ projects and contains a total of 79,496 samples. 
Each sample includes: 

	"prompt": The test prefix and the definition of the focal method (i.e., the method under test),
	"label": The corresponding test oracle （such as assertEqual(a, nullptr)）, and
	"score": A quality score based on multi-dimensional evaluation.

This dataset serves as the accompanying resource for the paper "AutoOracle: High-Quality C++ Test Oracle Generation via Data Quality-Driven and Filtering-Enabled LLMs", reflecting Samsung Electronics' latest research achievements in the field of automated testing for embedded software. It provides a standardized training and evaluation benchmark for C++ test oracle generation models, and offers strong support for test automation practices in industry sectors such as embedded systems and firmware development.
Dataset Construction Method (Optional):

We use the following key techniques to build a high-quality TAP dataset:

	Oracle De-Differentiation Method:
        Normalize logically equivalent oracles into a unified format to reduce style variations and improve data consistency.
	TAP Quality Scoring and Filtering Mechanism:
        Evaluate the relevance between TAPs and focal methods from multiple perspectives, and filter out low-quality samples to ensure reliable training data.

Directory Structure:

In the AutoOracle_Dataset:
1. data/AutoOracle_Dataset_train_1.json, data/AutoOracle_Dataset_train_2.json and data/AutoOracle_Dataset_test.json are the C++ training and testing datesets.
2. licenses/ORIGINAL_PROJECTS_LIST.txt:  this is the list of the open-source C++ projects downloaded from Github which we used to generate the dataset. It is including [project name + github url + license + copyright + notice files] info.
3. licenses/ORIGINAL_PROJECTS_LICENSE_TEXTS.txt:  this file is list up all the original license for the open-source C++ projects downloaded from Github which we used to generate the dataset.
4. licenses/notices/: under this folder there are the original notices files of the open-source C++ projects downloaded from Github which we used to generate the dataset.

Usage Suggestions:

	LLM Training / Fine-tuning:
        This dataset can be used to train or fine-tune large language models for C++ test oracle generation.	
	Model Evaluation:	
        It can be used to evaluate the performance of different test oracle generation approaches in the context of C++.
	Research Support:	
        The dataset provides a solid foundation for research in areas such as embedded systems and C++ software testing.

