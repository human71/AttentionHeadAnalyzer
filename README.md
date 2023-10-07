# AttentionHeadAnalyzer
The task involves assessing and ranking attention heads in the last layer of a language model based on their operational contribution using Few-shot In-context Learning and small perturbations.

<h3>Details</h3>h3>
Sort the attention heads in a decreasing order of the last layer based on their operational contribution. (use Few-shot In-context Learning). Please follow the steps in order to generate a attention head’s operational score:<br>
**Step 1:** Get access to the given dataset <br>
**Step 2:** Get a small size generative LM ( like GPT-Neo) <br>
**Step 3:** Evaluate the dataset and collect the performance scores, let’s call it result_original. <br>
**Step 4:** Now, for each attention head in the last layer <br>
&nbsp;&nbsp;&nbsp;&nbsp;**Step 4.1:** output(attention_head_i) += small noise<br>
&nbsp;&nbsp;&nbsp;&nbsp;**Step 4.2:** Propagate the noisy output of the attention_head_i <br>
&nbsp;&nbsp;&nbsp;&nbsp;**Step 4.3:** Evaluate the dataset. <br>
&nbsp;&nbsp;&nbsp;&nbsp;**Step 4.5:** Collect the performance scores, let’s call it result_atth_i<br>
**Step 5:** For each result_atth_i, measure the it’s deviation from the result_original.<br>
**Step 6:** Sort and print the output.<br>
