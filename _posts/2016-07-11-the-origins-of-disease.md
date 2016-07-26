---
published: false
---

## Model Driven Drug Discovery

Modern drug discovery is an artisanal pursuit, driven more by luck and
expert knowledge than by systematic discovery. While this approach has
worked spectacularly in the past, the last few years have seen a systematic
decrease in the number of new drugs discovered for dollar spent. [Eroom's
law](http://blogs.sciencemag.org/pipeline/archives/2012/03/08/erooms_law)
empirically demonstrates that the number of new drugs per dollar has been
falling exponentially. Eroom is of course Moore spelled backward, and the
opposite trends in computational power per dollar versus drugs discovered
per dollar serve as a reminder that naive computation is insufficient to
solve hard biological problems (a topic I've
[written](http://rbharath.github.io/the-ferocious-complexity-of-the-cell/)
about previously)

How can we change this state of affairs? I hypothesize that the best path
forward is to systematically create models of human disease and drug
actions. To explain this choice, let's take a quick detour into the history
of drug discovery. Early drug discovery was driven by [phenotypic
screening](https://en.wikipedia.org/wiki/Phenotypic_screening), in which
drugs were selected based on demonstrated efficacy in sick humans or
animals. While this approach was highly effective, it suffered from low
throughput; only a few sick humans or animals were available, making it
difficult to test many potential drugs. As a result, the pharmaceutical
industry increasingly shifted towards [targeted drug
discovery](https://en.wikipedia.org/wiki/Drug_discovery). Biologists'
increasing knowledge of the molecular mechanisms underlying life made it
possible to select out single types of molecules and hypothesize that a
disease could stopped by knocking such fault molecule. The targeted
approach also facilitated very large scale __in-vitro __ (in the test-tube)
experiments (since large batches of solution containing the faulty molecule
could be prepared easily), and made it possible discover unexpected
treatments using molecular similarities between various subsystems in the
body.

While the shift to targeted drug discovery facilitated many procedural
aspects, it also explains in large parts the drop in yield per dollar.
Biology is hard, and human understanding of the body's regulatory
mechanisms is highly incomplete and best, and completely wrong at worst.
Any pharmaceutical veteran can share stories where a potential molecule
looked highly promising in all early stage targeted tests, but caused
catastropic deaths in the first animal trials. The question for forward
progess then remains: how can we regain the efficacy of early phenotypic
screening, while retaining the scale and precision of targeted discovery
campaigns?

A number of innovative experimental solutions have started to mature. For
example, [PerlsteinLab](http://www.plab.co/) uses
[CRISPR](https://en.wikipedia.org/wiki/CRISPR) to make mutations in
non-mammalian organisms (such as nematodes or flies) to enable them to
better model human genetic disorders. This approach offers scale, since
non-mammalian organisms can often be raised to maturity quickly, allowing
for large scale testing of hypotheses. Other companies such as
  [Transcriptic](https://www.transcriptic.com/) or [Emerald Cloud
  Lab](http://emeraldcloudlab.com/) promise to facilitate complex
  biological experiments, allowing researchers to perform more sanity
  checks on their proposed drugs.

  While these advances will likely prove very useful, I suspect that in
  isolation, they won't be sufficient to regain the efficiency of
  systematic phenotypic screening. Any model is limited by human
  understanding of the biology underlying diseased systems, and our
  understanding remains too weak. As Donald Rumsfeld famously noted, it's
  hard to plan for unknown unknowns, in life and in drug discovery. What
  then is the path forward?

  I propose that we need to systematically learn algorithmic models of
  complex biological systems, capable of capturing insight not directly
  visible to human scientists. Although the pharmaceutical industry
  [routinely
  uses](https://en.wikipedia.org/wiki/Quantitative_structure%E2%80%93activity_relationship)
  simple statistical models of molecular properties such as solubility or
  toxicity to guide drug discovery,


  Furthermore, we Will require computational models of the immune system
  response, and should use real clinical data from electronic health care
  records to understand effects of drugs on human patients.

  In general, more models of the human body for drug discovery are needed.
  Currently have models of drug distribution, blood-brain barrier
  penetration, drug pKa, and metabolism. But, none of these models are
  stitched together into a model of the whole human. This limitation stands
  in contrast to animal models.

  To support our hypothesis, it helps to take a quick tour of common types
  of human diseases.
  To start, Bacterial infections are cured by flushing out all the bacteria
  from the body. Viral infections are also cured by flushing viruses out of
  the body. The problem is dealing with "viral reservoirs" that store parts
  of the disease even after the main viral bodies have been flushed. A big
  problem in finding a cure to AIDS.

  As opposed to infectious diseases, cancer is (mostly) a disease caused by
  local mutations (this statement is an oversimplification. Cancer can be
  infectious, transmitted by cancerous cells or viruses). Cancer is "cured"
  by flushing all the cancer cells out by killing them. In practice,
  remission rates remain high since not all cancer cells are killed.

  Immuno disorders (allergies, rheumatoid arthritis) appear to have
  behavioral causes. Lack of exposure to "dirty" environments might have
  caused these diseases. Many, many diseases look to be caused by
  immunological disorders, including Alzheimer's and the link.

  Obesity has no real cure. Diet and exercise help, but there appears to be
  a high rate of recidivism. Some rising evidence that microbiomes (the
  community of bacteria which naturally live in human intestines) may play
  critical roles in such disorders.

  Genetic disorders result from small mutations to critical genes. Often,
  single proteins cease to function properly, causing issues. Such
  disorders could potentially be cured by the rising tide of new genetic
  treatment therapies.

  Now that we have completed a basic tour of diseases, we can consider a
  basic tour of methods to cure these diseases. GWAS studies sequence
  thousands of patients and healthy people, and use a statistical model to
  find genomic variants correlated with the disease outcome. GWAS studies
  work excellently when a small number of genetic variants are strongly
  linked to the disease in question (CITE), but is much less useful when a
  large number of variants are loosely linked to the disorder (as is the
  case for diseases such as autism) (CITE).

  The basic strategy is to create a cell culture, a set of diseased cells
  which grow well in culture (that is in a plate containing agar). For
  cancer, a number of cancer cells lines have been created, which are cells
  harvested from cancerous tumours. Examples of such cell lines include the
  infamous HeLa cells (CITE). The major weakness of the cell culture
  approach is that it is never easy to verify that a particular cell
  culture comes from the source we believe. Cross contamination of
  cell-lines is a major problem here (CITE). The advent of cheaper
  sequencing might enable better quality control, by allowing researchers
  to regularly sequence their cell cultures to verify that they match the
  reference baseline. 

  Another weakness of cell culture data is that it is never clear if the
  induced response is merely an artifact of the cell residing in an
  unnatural growth medium. Tissues have cells arranged in more complex
  hierarchical formations, which themselves allow for more elaborate
  control structures between the cells (CITE). A recent improvement in this
  space is the advent of organoid models which grow cultures of cells into
  three dimensions pseudo-organs. This provides the hope of more accurate
  models which capture more of the disease biology.

  Knockout studies use gene editing in mice to test whether introducing or
  removing a gene causes onset or cure to the disease. The main advantage
  to this strategy is that it enables researchers to create a "model
  organism". That is, genetically modify or breed or infect animals
  (typically rats or mice) so that they have a version of the disease in
  question. Apply proposed treatments to said animals until one works. Move
  forward with that treatment to tests with human patients.

  This approach has many strengths. Since human understanding of biology is
  quite weak, it allows for testing biology with biology. The downside is
  that it's not easy to make animal models for more complex diseases, such
  as neurodegenerative diseases or mental disorders.

  I propose that the path forward is to systematically augment the use of
  animal models with computational disease  models. The thesis is to create
  models of disease using all available data from GWAS studies, animal
  models of the disease, and from clinical data. The computational model of
  the disease would then be tested with a prospective compound, and the
  constructed model must be capable of predicting the induced response.
  This induced response can be experimentally tested in one of the physical
  data sources, and the data obtained can be used to refine the
  computational disease model. This active learning loop would allow for
  fine tuning of the disease models.

  In this proposal, there would be a computational model of a tumor, or say
  of a bone-breakage, or of the patient pain. Predictions of treatments
  would proceed by testing against the model, and by filtering predicted
  outcomes with human insight from doctors. The advantage of this approach
  is that it provides an intellectual framework with which to approach
  personal medicine.



  Model Organoid reference:
  http://www.medicalnewstoday.com/articles/311599.php
