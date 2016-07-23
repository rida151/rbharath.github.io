---
published: false
---
## Model Driven Drug Discovery

Modern drug discovery is an artisanal pursuit, driven more by luck and expert knowledge than by systematic discovery. How can we change this state of affairs? I hypothesize that we need better models of disease to find better drugs. CRISPR driven animal models will become very important. Computational disease modeling will also become more important, especially for diseases where it is not feasible to build animal models with current technology.

Furthermore, we Will require computational models of the immune system response, and should use real clinical data from electronic health care records to understand effects of drugs on human patients.

In general, more models of the human body for drug discovery are needed. Currently have models of drug distribution, blood-brain barrier penetration, drug pKa, and metabolism. But, none of these models are stitched together into a model of the whole human. This limitation stands in contrast to animal models.

To support our hypothesis, it helps to take a quick tour of common types of human diseases.
To start, Bacterial infections are cured by flushing out all the bacteria from the body. Viral infections are also cured by flushing viruses out of the body. The problem is dealing with "viral reservoirs" that store parts of the disease even after the main viral bodies have been flushed. A big problem in finding a cure to AIDS.

As opposed to infectious diseases, cancer is (mostly) a disease caused by local mutations (this statement is an oversimplification. Cancer can be infectious, transmitted by cancerous cells or viruses). Cancer is "cured" by flushing all the cancer cells out by killing them. In practice, remission rates remain high since not all cancer cells are killed.

Immuno disorders (allergies, rheumatoid arthritis) appear to have behavioral causes. Lack of exposure to "dirty" environments might have caused these diseases. Many, many diseases look to be caused by immunological disorders, including Alzheimer's and the link.

Obesity has no real cure. Diet and exercise help, but there appears to be a high rate of recidivism. Some rising evidence that microbiomes (the community of bacteria which naturally live in human intestines) may play critical roles in such disorders.

Genetic disorders result from small mutations to critical genes. Often, single proteins cease to function properly, causing issues. Such disorders could potentially be cured by the rising tide of new genetic treatment therapies.

Now that we have completed a basic tour of diseases, we can consider a basic tour of methods to cure these diseases. GWAS studies sequence thousands of patients and healthy people, and use a statistical model to find genomic variants correlated with the disease outcome. GWAS studies work excellently when a small number of genetic variants are strongly linked to the disease in question (CITE), but is much less useful when a large number of variants are loosely linked to the disorder (as is the case for diseases such as autism) (CITE).

Knockout studies use gene editing in mice to test whether introducing or removing a gene causes onset or cure to the disease. The main advantage to this strategy is that it enables researchers to create a "model organism". That is, genetically modify or breed or infect animals (typically rats or mice) so that they have a version of the disease in question. Apply proposed treatments to said animals until one works. Move forward with that treatment to tests with human patients.

This approach has many strengths. Since human understanding of biology is quite weak, it allows for testing biology with biology. The downside is that it's not easy to make animal models for more complex diseases, such as neurodegenerative diseases or mental disorders.

An improvement in this space is the advent of organoid models which grow cultures of cells into three dimensions pseudo-organs.

Model Organoid reference: http://www.medicalnewstoday.com/articles/311599.php