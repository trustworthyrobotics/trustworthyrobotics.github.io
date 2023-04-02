---
layout: page
title: Projects
permalink: /projects/
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

<!-- <hr> -->
<br>
## Reliable planning with learned models
<hr>
<br>

Using learned perception and dynamics models in the autonomy pipeline can reduce requirements on <em>a priori</em> knowledge. However, these models often fail to generalize when deployed in domains which they have not seen in training; thus, blindly trusting these models in planning may lead to unsafe and unpredictable runtime behavior. This project seeks to quantify where and to what extent these learned models can be trusted, in order to plan trajectories which ensure that the robot will behave safely and reliably at runtime. Achieving this requires an integrated, end-to-end verification of the system, all the way from perception to low-level feedback control.

### <span style="font-weight:bold"> Selected publications:</span><br>

<table class="table">
<colgroup>
	<col width="30%" />
	<col width="2%" />
	<col width="68%" />
</colgroup>
<tbody>


<tr id="Knuth23b">
	<td markdown="span"><br><img src="../images/icra_23b_01.png" onmouseover="this.src='../images/icra_23b_02.gif'" onmouseout="this.src='../images/icra_23b_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Statistical Safety and Robustness Guarantees for Feedback Motion Planning of Unknown Underactuated Stochastic Systems** <br> 
		<em>Craig Knuth, **Glen Chou**, Jamie Reese, Joseph Moore</em> <br> 
		Proceedings of the 60th IEEE International Conference on Robotics and Automation (ICRA), May 2023. <br>
		[<a href="javascript:toggleInfo(&#39;Knuth23b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Knuth23b&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2212.06874)\] \[<a href="https://arxiv.org/pdf/2212.06874.pdf">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Knuth23b&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Knuth23b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for providing statistical guarantees on runtime safety and goal reachability for integrated planning and control of a class of systems with unknown nonlinear stochastic underactuated dynamics. Specifically, given a dynamics dataset, our method jointly learns a mean dynamics model, a spatially-varying disturbance bound that captures the effect of noise and model mismatch, and a feedback controller based on contraction theory that stabilizes the learned dynamics. We propose a sampling-based planner that uses the mean dynamics model and simultaneously bounds the closed-loop tracking error via a learned disturbance bound. We employ techniques from Extreme Value Theory (EVT) to estimate, to a specified level of confidence, several constants which characterize the learned components and govern the size of the tracking error bound. This ensures plans are guaranteed to be safely tracked at runtime. We validate that our guarantees translate to empirical safety in simulation on a 10D quadrotor, and in the real world on a physical CrazyFlie quadrotor and Clearpath Jackal robot, whereas baselines that ignore the model error and stochasticity are unsafe. </div></td>
  </tr>
<tr id="bib_Knuth23b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Knuth-ICRA-23,<br>   Author = "Craig Knuth, Glen Chou, Jamie Reese, and Joseph Moore",
   journal = {Proceedings of the 60th IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "Statistical Safety and Robustness Guarantees for Feedback Motion Planning of Unknown Underactuated Stochastic Systems",<br>   year = {2023}<br>}</pre></td>
</tr>

<tr id="Chou22b">
	<td markdown="span"><br><img src="../images/wafr_22_01.jpg" onmouseover="this.src='../images/wafr_22_02.gif'" onmouseout="this.src='../images/wafr_22_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Safe Output Feedback Motion Planning from Images via Learned Perception Modules and Contraction Theory** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of the 15th International Workshop on the Algorithmic Foundations of Robotics (WAFR), June 2022. <br>
		[<a href="javascript:toggleInfo(&#39;Chou22b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou22b&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2206.06553)\] \[<a href="https://doi.org/10.1007/978-3-031-21090-7_21">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=yNKyBgj0cIE">Talk</a>\] [<a href="javascript:toggleInfo(&#39;Chou22b&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou22b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a motion planning algorithm for a class of uncertain control-affine nonlinear systems which guarantees runtime safety and goal reachability when using high-dimensional sensor measurements (e.g., RGB-D images) and a learned perception module in the feedback control loop. First, given a dataset of states and observations, we train a perception system that seeks to invert a subset of the state from an observation, and estimate an upper bound on the perception error which is valid with high probability in a trusted domain near the data. Next, we use contraction theory to design a stabilizing state feedback controller and a convergent dynamic state observer which uses the learned perception system to update its state estimate. We derive a bound on the trajectory tracking error when this controller is subjected to errors in the dynamics and incorrect state estimates. Finally, we integrate this bound into a sampling-based motion planner, guiding it to return trajectories that can be safely tracked at runtime using sensor data. We demonstrate our approach in simulation on a 4D car, a 6D planar quadrotor, and a 17D manipulation task with RGB(-D) sensor measurements, demonstrating that our method safely and reliably steers the system to the goal, while baselines that fail to consider the trusted domain or state estimation errors can be unsafe. </div></td>
  </tr>
<tr id="bib_Chou22b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-WAFR-22,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of the 15th International Workshop on the Algorithmic Foundations of Robotics (WAFR)},<br>   Title = "Safe Output Feedback Motion Planning from Images via Learned Perception Modules and Contraction Theory",<br>   year = {2022}<br>}</pre></td>
</tr>

<tr id="Chou21c">
	<td markdown="span"><img src="../images/cdc_21_02.png" onmouseover="this.src='../images/cdc_21_01.png'" onmouseout="this.src='../images/cdc_21_02.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span">**Model Error Propagation via Learned Contraction Metrics for Safe Feedback Motion Planning of Unknown Systems** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of the 60th IEEE Conference on Decision and Control (CDC), December 2021. <br>
		[<a href="javascript:toggleInfo(&#39;Chou21c&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou21c&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2104.08695)\] \[<a href="https://doi.org/10.1109/CDC45484.2021.9683354">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=DYEyD5y-2po">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Chou21c&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou21c" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for contraction-based feedback motion planning of locally incrementally exponentially stabilizable systems with unknown dynamics that provides probabilistic safety and reachability guarantees. Given a dynamics dataset, our method learns a deep control-affine approximation of the dynamics. To find a trusted domain where this model can be used for planning, we obtain an estimate of the Lipschitz constant of the model error, which is valid with a given probability, in a region around the training data, providing a local, spatially-varying model error bound. We derive a trajectory tracking error bound for a contraction-based controller that is subjected to this model error, and then learn a controller that optimizes this tracking bound. With a given probability, we verify the correctness of the controller and tracking error bound in the trusted domain. We then use the trajectory error bound together with the trusted domain to guide a sampling-based planner to return trajectories that can be robustly tracked in execution. We show results on a 4D car, a 6D quadrotor, and a 22D deformable object manipulation task, showing our method plans safely with learned models of high-dimensional underactuated systems, while baselines that plan without considering the tracking error bound or the trusted domain can fail to stabilize the system and become unsafe. </div></td>
  </tr>
<tr id="bib_Chou21c" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-CDC-21,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of the 60th IEEE Conference on Decision and Control (CDC)},<br>   Title = "Model Error Propagation via Learned Contraction Metrics for Safe Feedback Motion Planning of Unknown Systems",<br>   year = {2021}<br>}</pre></td>
</tr>



<tr id="Knuth21a">
	<td markdown="span"><br><img src="../images/ral_21_01.jpg" onmouseover="this.src='../images/ral_21_02.gif'" onmouseout="this.src='../images/ral_21_01.jpg'" /> <br>  </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Planning with Learned Dynamics: Probabilistic Guarantees on Safety and Reachability via Lipschitz Constants** <br> 
		<em>Craig Knuth\*, **Glen Chou\***, Necmiye Ozay, Dmitry Berenson</em> <br> 
		IEEE Robotics and Automation Letters (RA-L), with presentation at ICRA 2021, vol. 6, no. 3, pp. 5129-5136, July 2021. <br>
		[<a href="javascript:toggleInfo(&#39;Knuth21a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Knuth21a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2010.08993)\] \[<a href="https://doi.org/10.1109/LRA.2021.3068889">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=Bk5S_UByAqM">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Knuth21a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Knuth21a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for feedback motion planning of systems with unknown dynamics which provides probabilistic guarantees on safety, reachability, and goal stability. To find a domain in which a learned control-affine approximation of the true dynamics can be trusted, we estimate the Lipschitz constant of the difference between the true and learned dynamics, and ensure the estimate is valid with a given probability. Provided the system has at least as many controls as states, we also derive existence conditions for a one-step feedback law which can keep the real system within a small bound of a nominal trajectory planned with the learned dynamics. Our method imposes the feedback law existence as a constraint in a sampling-based planner, which returns a feedback policy around a nominal plan ensuring that, if the Lipschitz constant estimate is valid, the true system is safe during plan execution, reaches the goal, and is ultimately invariant in a small set about the goal. We demonstrate our approach by planning using learned models of a 6D quadrotor and a 7DOF Kuka arm. We show that a baseline which plans using the same learned dynamics without considering the error bound or the existence of the feedback law can fail to stabilize around the plan and become unsafe. </div></td>
  </tr>
<tr id="bib_Knuth21a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Knuth-RAL-21,<br>   Author = "Craig Knuth*, Glen Chou*, Necmiye Ozay, and Dmitry Berenson",
   journal = {IEEE Robotics and Automation Letters (RA-L)},<br>   Title = "Planning with Learned Dynamics: Probabilistic Guarantees on Safety and Reachability via Lipschitz Constants",<br>   year = {2021}<br>}</pre></td>
</tr>



</tbody>
</table>
<!-- <hr> -->

<br>

## Learning task specifications from demonstrations

<hr>
<br>
A key input to a motion planner is the set of constraints that define the task that must be completed (the task specification). These can involve high-level constraints, e.g., "fill the glass of water before delivering it", as well as low-level constraints, e.g., "don't tip the filled glass more than 15 degrees from the upright position". For complex tasks, it can be challenging for robot end-users to specify such constraints; a more natural approach is to demonstrate the task. In this project, we seek to use demonstrations to infer the set of constraints that must be met in order for the task to be safely completed, by using results from optimization theory. We also design methods for planning safely with these learned task specifications in spite of the uncertainty in the learned constraints.

### <span style="font-weight:bold"> Selected publications:</span><br>

<table class="table">
<colgroup>
	<col width="30%" />
	<col width="2%" />
	<col width="68%" />
</colgroup>
<tbody>


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

