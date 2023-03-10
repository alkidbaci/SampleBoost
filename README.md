# SampleBoost

SampleBoost is a framework for accelerating concept learning with sampling.
We have implemented our code inside the library [Ontolearn](https://github.com/dice-group/Ontolearn/tree/develop)
inside the folder named [Sampling](https://github.com/alkidbaci/SampleBoost/tree/main/Sampling).


## Getting started

There are 3 methods to generate the result starting with the most general.

1.  The evaluation results for a certain sampling percentage can be simply reproduced by running `evaluation_table_generator.py`.
    There are a few adjustable variables as following:
    - `datasets_path` -> list containing the name of the json files that contains the path to the knowledge graph and
                               the learning problem.
    - `samplers` -> list of the abbreviation of the samplers as strings.
    - `sampling_percentage` -> the sampling percentage
    - `x` -> number of iterations for each sampler ( default value 50 )

    > **Note**: Keep in mind that this file needs a considerable time to execute ( more than 2 hours).
             The edge samplers are not included in this file because they sample depending on edges. You can use the other
             evaluation methods described below to reproduce the evaluation results for random edge samplers.

2.  To perform the evaluation only for a single sampler in multiple samples, run `sampling_multiple_run_performance_display.py`.
    There are a few adjustable variables as following:
    - name of the json file (enter directly in line 30)
    - `sampler` -> the sampler object
    - `x` -> number of nodes to sample

3.  To evaluate a single sampler only in a single sample, run `sampling_single_run_performance_display.py`.
    There are a few adjustable variables as following:
    - name of the json file (enter directly in line 29)
    - `sampler` -> the sampler object

### Questions?

Feel free to email [alkid1baci@gmail.com](mailto:alkid1baci@gmail.com)
if questions arise.