# system-prompt-exfiltration-detection
The rapid adoption of large language models (LLMs) has introduced many challenges in safeguarding LLM-based
applications against various risks. One critical threat is system prompt leakage, where an attacker manipulates
the model to reveal its internal instructions. Such leaks can lead to privacy violations, unauthorized access, and
exploitation of proprietary logic. Recent literature on this type of attacks overlooks many diverse ways in which
sensitive information can be exposed to the attacker. Existing studies on leak detection predominantly focus
on threshold-based detection using single substring match measures, which can easily miss many other forms
in which leaks can happen. Moreover, there is no single comprehensive definition of what exactly constitutes
information leakage in general. System prompt leakage has gained a lot of attention in the past months, however,
many of the new methods do not demonstrate robustness against easiest edge cases. This work introduces a
more nuanced approach to prompt leak detection by stepping back and investigating the underlying challenge
behind information leakage: what does it take to conclude that one piece of text is similar enough to another
that it can be considered a leak? Based on the conclusions, we curate a set of text similarity metrics and create
a system prompt leak dataset that includes diverse categories of exfiltration. Most importantly, this work walks
through the process of training a decision tree-based classifier that can serve as an output filter for prompt
leakage. Our classifier shows remarkable results and generalizability, achieving a 89% accuracy and f1-score,
and 98% prompt leak recall rate on an external dataset.
