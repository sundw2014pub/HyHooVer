# HyHooVer: Verification and Parameter Synthesis in Stochastic Systems with Hybrid State-space using Optimistic Optimization

A model-free verification of a general class of control system with unknown nonlinear hybrid dynamics, where the state-space has both a continuum and a discrete component.



# Usage

```
usage: check.py [-h] [--model MODEL] [--args ARGS [ARGS ...]] [--nRuns NRUNS]
                [--budget BUDGET] [--rho_max RHO_MAX] [--sigma SIGMA]
                [--nHOOs NHOOS] [--batch_size BATCH_SIZE] [--output OUTPUT]
                [--seed SEED] [--eval_mult EVAL_MULT] [--eval]
                [--init INIT [INIT ...]] [--rnd_sampling]

optional arguments:
  -h, --help            show this help message and exit
  --model MODEL         models available: Roundabout (default: Synthetic)
  --args ARGS [ARGS ...]
                        <Optional> this can be used to pass special arguments
                        to the model (for instance for Synthetic example I use
                        args to pass number of modes and the dimension of the
                        states).
  --nRuns NRUNS         number of repetitions. (default: 1)
  --budget BUDGET       sampling budget for total number of simulations
                        (including final evaluation). (default: 1000)
  --rho_max RHO_MAX     smoothness parameter. (default: 0.95)
  --sigma SIGMA         <Optional> sigma parameter used in UCB. If not
                        specified, it will be sqrt(0.5*0.5/batch_size).
  --nHOOs NHOOS         number of HyHOO instances to use. (default: 1)
  --batch_size BATCH_SIZE
                        batch size parameter. (default: 10)
  --output OUTPUT       file name to save the results. (default:
                        ./output_synthetic.dat)
  --seed SEED           random seed for reproducibility. (default: 1024)
  --eval_mult EVAL_MULT
                        sampling budget for final evaluation by Monte_carlo
                        simulations. (default: 100)
  --eval
  --init INIT [INIT ...]
                        <Optional> this can be used to evaluate a specific
                        initial state or parameter.
  --rnd_sampling        <Optional> this can be used to specify whether to
                        sample from the geometric center of a region or sample
                        randomly. (default: False)
```



# Acknowledgements

The MFTreeSearchCV code base was developed by Rajat Sen: ( https://github.com/rajatsen91/MFTreeSearchCV ) which in-turn was built on the blackbox optimization code base of Kirthivasan Kandasamy: ( https://github.com/kirthevasank )

