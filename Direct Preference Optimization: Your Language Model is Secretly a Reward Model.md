# Direct Preference Optimization:
## Your Language Model is Secretly a Reward Model
Rafael Rafailov∗† Archit Sharma∗† Eric Mitchell∗†
Stefano Ermon†‡ Christopher D. Manning† Chelsea Finn†
†Stanford University ‡CZ Biohub
{rafailov,architsh,eric.mitchell}@cs.stanford.edu

### Abstract :
While large-scale unsupervised language models (LMs) learn broad world knowledge and some reasoning skills, achieving precise control of their behavior is
difficult due to the completely unsupervised nature of their training. Existing
methods for gaining such steerability collect human labels of the relative quality of
model generations and fine-tune the unsupervised LM to align with these preferences, often with reinforcement learning from human feedback (RLHF). However,
RLHF is a complex and often unstable procedure, first fitting a reward model that
reflects the human preferences, and then fine-tuning the large unsupervised LM
using reinforcement learning to maximize this estimated reward without drifting
too far from the original model. In this paper, we leverage a mapping between
reward functions and optimal policies to show that this constrained reward maximization problem can be optimized exactly with a single stage of policy training,
essentially solving a classification problem on the human preference data. The
resulting algorithm, which we call Direct Preference Optimization (DPO), is stable,
performant, and computationally lightweight, eliminating the need for fitting a
reward model, sampling from the LM during fine-tuning, or performing significant
hyperparameter tuning. Our experiments show that DPO can fine-tune LMs to
align with human preferences as well as or better than existing methods. Notably,
fine-tuning with DPO exceeds RLHF’s ability to control sentiment of generations
and improves response quality in summarization and single-turn dialogue while
being substantially simpler to implement and train.
