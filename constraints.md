---
layout: page
title: Safely Learning Task Specifications from Humans
permalink: /projects/constraints
---

<script type="text/javascript">
function toggleInfo(articleid,info) {

	var entry = document.getElementById(articleid);
	var abs = document.getElementById('abs_'+articleid);
	var bib = document.getElementById('bib_'+articleid);
	var notes = document.getElementById('notes_'+articleid);

	if (abs && info == 'abstract') {
		if(abs.className.indexOf('abstract') != -1) {
		abs.className.indexOf('noshow') == -1?abs.className = 'abstract noshow':abs.className = 'abstract';
		}
	} else if (bib && info == 'bibtex') {
		if(bib.className.indexOf('bibtex') != -1) {
		bib.className.indexOf('noshow') == -1?bib.className = 'bibtex noshow':bib.className = 'bibtex';
		}
	} else if (notes && info == 'notes') {
		if(notes.className.indexOf('notes') != -1) {
		notes.className.indexOf('noshow') == -1?notes.className = 'notes noshow':notes.className = 'notes';
		}
	}
	 else {
		return;
	}

	// check if one or the other is available
	var absshow = false;
	var bibshow = false;
	var notesshow = false;
	(abs && abs.className.indexOf('noshow') == -1)? absshow = true: absshow = false;
	(bib && bib.className == 'bibtex')? bibshow = true: bibshow = false;
	(notes && notes.className == 'notes')? notesshow = true: notes = false;

	// highlight original entry
	if(entry) {
		if (absshow || bibshow || notesshow) {
		entry.className = 'entry highlight show';
		} else {
		entry.className = 'entry show';
		}
	}

	// When there's a combination of abstract/review/bibtex showing, need to add class for correct styling
	if(absshow) {
		(bibshow)?abs.className = 'abstract nextshow':abs.className = 'abstract';
	}
}
</script>


A key input to a motion planner is the set of constraints that define the task that must be completed (the task specification). These can involve high-level constraints, e.g., "fill the glass of water before delivering it", as well as low-level constraints, e.g., "don't tip the filled glass more than 15 degrees from the upright position". For complex tasks, it can be challenging for robot end-users to specify such constraints; a more natural approach is to demonstrate the task or provide an instruction in natural language (NL). In this work, we seek to use demonstrations to infer the set of constraints that must be met in order for the task to be safely completed, by using results from optimization theory. We also design methods for planning safely with these learned task specifications, which can represent complex multi-stage tasks expressed in, e.g., linear temporal logic (LTL), in spite of the uncertainty in the learned specification. More recently, we have leveraged LLMs for data-efficient training of NL-to-LTL translators, enabling safer planning with less than a dozen human labels.

### <span style="font-weight:bold"> Selected publications:</span><br>

<table class="table">
<colgroup>
	<col width="30%" />
	<col width="2%" />
	<col width="68%" />
</colgroup>
<tbody>


<tr id="Pan23a">
	<td markdown="span"><br><img src="../images/icra_23a_01.png" onmouseover="this.src='../images/icra_23a_02.png'" onmouseout="this.src='../images/icra_23a_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Data-Efficient Learning of Natural Language to Linear Temporal Logic Translators for Robot Task Specification** <br> 
		<em>Jiayi Pan, **Glen Chou**, Dmitry Berenson</em> <br> 
		Proceedings of the 60th IEEE International Conference on Robotics and Automation (ICRA), May 2023. <br>
		[<a href="javascript:toggleInfo(&#39;Pan23a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Pan23a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2303.08006)\] \[<a href="https://arxiv.org/pdf/2303.08006.pdf">PDF</a>\] \[<a href="https://www.youtube.com/watch?v=gkSGI7hNerA">Supplementary Video</a>\] \[<a href="https://github.com/UM-ARM-Lab/Efficient-Eng-2-LTL">Code</a>\] [<a href="javascript:toggleInfo(&#39;Pan23a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Pan23a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: To make robots accessible to a broad audience, it is critical to endow them with the ability to take universal modes of communication, like commands given in natural language, and extract a concrete desired task specification, defined using a formal language like linear temporal logic (LTL). In this paper, we present a learning-based approach for translating from natural language commands to LTL specifications with very limited human-labeled training data. This is in stark contrast to existing natural-language to LTL translators, which require large human-labeled datasets, often in the form of labeled pairs of LTL formulas and natural language commands, to train the translator. To reduce reliance on human data, our approach generates a large synthetic training dataset through algorithmic generation of LTL formulas, conversion to structured English, and then exploiting the paraphrasing capabilities of modern large language models (LLMs) to synthesize a diverse corpus of natural language commands corresponding to the LTL formulas. We use this generated data to finetune an LLM and apply a constrained decoding procedure at inference time to ensure the returned LTL formula is syntactically correct. We evaluate our approach on three existing LTL/natural language datasets and show that we can translate natural language commands at 75% accuracy with far less human data (≤12 annotations). Moreover, when training on large human-annotated datasets, our method achieves higher test accuracy (95% on average) than prior work. Finally, we show the translated formulas can be used to plan long-horizon, multi-stage tasks on a 12D quadrotor. </div></td>
  </tr>
<tr id="bib_Pan23a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Pan-ICRA-23,<br>   Author = "Jiayi Pan, Glen Chou, and Dmitry Berenson",
   journal = {Proceedings of the 60th IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "Data-Efficient Learning of Natural Language to Linear Temporal Logic Translators for Robot Task Specification",<br>   year = {2023}<br>}</pre></td>
</tr>



<tr id="Chou21b">
	<td markdown="span"><img src="../images/auro_22_01.jpg" onmouseover="this.src='../images/auro_22_02.gif'" onmouseout="this.src='../images/auro_22_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span">**Learning Temporal Logic Formulas from Suboptimal Demonstrations: Theory and Experiments** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Autonomous Robots (AURO), vol. 46, no. 1, pp. 149-174, January 2022. <br>
		[<a href="javascript:toggleInfo(&#39;Chou21b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou20a&#39;); ">Abstract</a>]
                 \[<a href="https://doi.org/10.1007/s10514-021-10004-x">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=xjlXpF_s3jY">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Chou21b&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou21b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for learning multi-stage tasks from demonstrations by learning the logical structure and atomic propositions of a consistent linear temporal logic (LTL) formula. The learner is given successful but potentially suboptimal demonstrations, where the demonstrator is optimizing a cost function while satisfying the LTL formula, and the cost function is uncertain to the learner. Our algorithm uses the Karush-Kuhn-Tucker (KKT) optimality conditions of the demonstrations together with a counterexample-guided falsification strategy to learn the atomic proposition parameters and logical structure of the LTL formula, respectively. We provide theoretical guarantees on the conservativeness of the recovered atomic proposition sets, as well as completeness in the search for finding an LTL formula consistent with the demonstrations. We evaluate our method on high-dimensional nonlinear systems by learning LTL formulas explaining multi-stage tasks on a simulated 7-DOF arm and a quadrotor, and show that it outperforms competing methods for learning LTL formulas from positive examples. Finally, we demonstrate that our approach can learn a real-world multi-stage tabletop manipulation task on a physical 7-DOF Kuka iiwa arm. </div></td>
  </tr>
  <tr id="bib_Chou21b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-AURO-21,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Autonomous Robots (AURO)},<br>   Title = "Learning Temporal Logic Formulas from Suboptimal Demonstrations: Theory and Experiments",<br>   year = {2022}<br>}</pre></td>
</tr>


<tr id="Chou20c">
	<td markdown="span"><br><img src="../images/corl_20_01.png" onmouseover="this.src='../images/corl_20_02.gif'" onmouseout="this.src='../images/corl_20_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Uncertainty-Aware Constraint Learning for Adaptive Safe Motion Planning from Demonstrations** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of the 4th Conference on Robot Learning (CoRL), November 2020. <br>
		[<a href="javascript:toggleInfo(&#39;Chou20c&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou20c&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2011.04141)\] \[<a href="https://proceedings.mlr.press/v155/chou21a.html">PDF</a>\] \[<a href="https://www.youtube.com/watch?v=u2zDKOQqAlQ">Talk</a>\] \[<a href="https://www.youtube.com/watch?v=aWZ_U-gWQJI">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Chou20c&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou20c" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for learning to satisfy uncertain constraints from demonstrations. Our method uses robust optimization to obtain a belief over the potentially infinite set of possible constraints consistent with the demonstrations, and then uses this belief to plan trajectories that trade off performance with satisfying the possible constraints. We use these trajectories in a closed-loop policy that executes and replans using belief updates, which incorporate data gathered during execution. We derive guarantees on the accuracy of our constraint belief and probabilistic guarantees on plan safety. We present results on a 7-DOF arm and 12D quadrotor, showing our method can learn to satisfy high-dimensional (up to 30D) uncertain constraints, and outperforms baselines in safety and efficiency. </div></td>
  </tr>
<tr id="bib_Chou20c" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-CoRL-20,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of the 4th Conference on Robot Learning (CoRL)},<br>   Title = "Uncertainty-Aware Constraint Learning for Adaptive Safe Motion Planning from Demonstrations",<br>   year = {2020}<br>}</pre></td>
</tr>



<tr id="Chou20a">
	<td markdown="span"><br><img src="../images/ral_20_01.jpg" onmouseover="this.src='../images/ral_20_02.gif'" onmouseout="this.src='../images/ral_20_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Constraints from Locally-Optimal Demonstrations under Cost Function Uncertainty** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		IEEE Robotics and Automation Letters (RA-L), with presentation at ICRA 2020, vol. 5, no. 2, pp. 3682-3690, April 2020. <br>
		[<a href="javascript:toggleInfo(&#39;Chou20a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou20a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2001.09336)\] \[<a href="https://doi.org/10.1109/LRA.2020.2974427">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=TM6DKFmRCIc">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Chou20a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou20a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present an algorithm for learning parametric constraints from locally-optimal demonstrations, where the cost function being optimized is uncertain to the learner. Our method uses the Karush-Kuhn-Tucker (KKT) optimality conditions of the demonstrations within a mixed integer linear program (MILP) to learn constraints which are consistent with the local optimality of the demonstrations, by either using a known constraint parameterization or by incrementally growing a parameterization that is consistent with the demonstrations. We provide theoretical guarantees on the conservativeness of the recovered safe/unsafe sets and analyze the limits of constraint learnability when using locally-optimal demonstrations. We evaluate our method on high-dimensional constraints and systems by learning constraints for 7-DOF arm and quadrotor examples, show that it outperforms competing constraint-learning approaches, and can be effectively used to plan new constraint-satisfying trajectories in the environment. </div></td>
  </tr>
<tr id="bib_Chou20a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-RAL-20,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {IEEE Robotics and Automation Letters (RA-L)},<br>   Title = "Learning Constraints from Locally-Optimal Demonstrations under Cost Function Uncertainty",<br>   year = {2020}<br>}</pre></td>
</tr>


</tbody>
</table>
<!-- <hr> -->

<br>

