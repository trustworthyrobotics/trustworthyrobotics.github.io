---
layout: page
title: Publications
permalink: /publications/
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
## Journal Papers
<hr>

<table class="table">
<colgroup>
	<col width="25%" />
	<col width="2%" />
	<col width="73%" />
</colgroup>
<tbody>

<tr id="Chou22a">
	<td markdown="span"><br><img src="../images/ral_22_01.jpg" onmouseover="this.src='../images/ral_22_02.gif'" onmouseout="this.src='../images/ral_22_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Gaussian Process Constraint Learning for Scalable Chance-Constrained Motion Planning From Demonstrations** <br> 
		<em>**Glen Chou\***, Hao Wang\*, Dmitry Berenson</em> <br> 
		IEEE Robotics and Automation Letters (RA-L), with presentation at ICRA 2022, vol. 7, no. 2, pp. 3827-3834, April 2022. <br>
		[<a href="javascript:toggleInfo(&#39;Chou22a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou22a&#39;); ">Abstract</a>]
                 \[[arXiv](https://arxiv.org/abs/2112.04612)\] \[<a href="https://doi.org/10.1109/LRA.2022.3148436">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=mN1X_2R9EtQ">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Chou22a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou22a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We propose a method for learning constraints represented as Gaussian processes (GPs) from locally-optimal demonstrations. Our approach uses the Karush-Kuhn-Tucker (KKT) optimality conditions to determine where on the demonstrations the constraint is tight, and a scaling of the constraint gradient at those states. We then train a GP representation of the constraint which is consistent with and which generalizes this information. We further show that the GP uncertainty can be used within a kinodynamic RRT to plan probabilistically-safe trajectories, and that we can exploit the GP structure within the planner to exactly achieve a specified safety probability. We demonstrate our method can learn complex, nonlinear constraints demonstrated on a 5D nonholonomic car, a 12D quadrotor, and a 3-link planar arm, all while requiring minimal prior information on the constraint. Our results suggest the learned GP constraint is accurate, outperforming previous constraint learning methods that require more a priori knowledge. </div></td>
  </tr>
  <tr id="bib_Chou22a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-RAL-22,<br>   Author = "Glen Chou, Hao Wang, and Dmitry Berenson",
   journal = {IEEE Robotics and Automation Letters (RA-L)},<br>   Title = "Gaussian Process Constraint Learning for Scalable Chance-Constrained Motion Planning From Demonstrations",<br>   year = {2022}<br>}</pre></td>
</tr>




<tr id="Chou21b">
	<td markdown="span"><br><img src="../images/auro_22_01.jpg" onmouseover="this.src='../images/auro_22_02.gif'" onmouseout="this.src='../images/auro_22_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Temporal Logic Formulas from Suboptimal Demonstrations: Theory and Experiments** <br> 
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




  <tr id="Chou21a">
  	<td markdown="span"><br><img src="../images/ijrr_21_01.png" onmouseover="this.src='../images/ijrr_21_02.png'" onmouseout="this.src='../images/ijrr_21_01.png'" />   </td>
  	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Constraints from Demonstrations with Grid and Parametric Representations** <br> 
		<em>**Glen Chou**, Dmitry Berenson, Necmiye Ozay</em> <br> 
		International Journal of Robotics Research (IJRR), vol. 40, no. 10-11, pp. 1255-1283, September 2021. <br>
		[<a href="javascript:toggleInfo(&#39;Chou21a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou20a&#39;); ">Abstract</a>]
                \[<a href="https://doi.org/10.1177/02783649211035177">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Chou21a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou21a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We extend the learning from demonstration paradigm by providing a method for learning unknown constraints shared across tasks, using demonstrations of the tasks, their cost functions, and knowledge of the system dynamics and control constraints. Given safe demonstrations, our method uses hit-and-run sampling to obtain lower cost, and thus unsafe, trajectories. Both safe and unsafe trajectories are used to obtain a consistent representation of the unsafe set via solving an integer program. Our method generalizes across system dynamics and learns a guaranteed subset of the constraint. Additionally, by leveraging a known parameterization of the constraint, we modify our method to learn parametric constraints in high dimensions. We also provide theoretical analysis on what subset of the constraint and safe set can be learnable from safe demonstrations. We demonstrate our method on linear and nonlinear system dynamics, show that it can be modiﬁed to work with suboptimal demonstrations, and that it can also be used to learn constraints in a feature space. </div></td>
  </tr>
  <tr id="bib_Chou21a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-IJRR-21,<br>   Author = "Glen Chou, Dmitry Berenson, and Necmiye Ozay",
   journal = {International Journal of Robotics Research (IJRR)},<br>   Title = "Learning Constraints from Demonstrations with Grid and Parametric Representations",<br>   year = {2021}<br>}</pre></td>
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
  <pre>@inproceedings{Knuth-RAL-21,<br>   Author = "Craig Knuth, Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {IEEE Robotics and Automation Letters (RA-L)},<br>   Title = "Planning with Learned Dynamics: Probabilistic Guarantees on Safety and Reachability via Lipschitz Constants",<br>   year = {2021}<br>}</pre></td>
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





<tr id='Chou18b'>
	<td markdown="span"><img src="../images/emsoft_18_01.png" onmouseover="this.src='../images/emsoft_18_02.png'" onmouseout="this.src='../images/emsoft_18_01.png'" />   </td>
	<td markdown="span"></td>
		<td markdown="span"><br>**Using control synthesis to generate corner cases: A case study on autonomous driving** <br> 
		<em>**Glen Chou**\*, Yunus E. Sahin\*, Liren Yang\*, Kwesi J. Rutledge, Petter Nilsson, Necmiye Ozay</em> <br> 
		IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (ESWEEK-TCAD special issue), vol. 37, no. 11, pp. 2906-2917, November 2018. <br>
		[<a href="javascript:toggleInfo(&#39;Chou18b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou18c&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/1807.09537)\] \[<a href="https://doi.org/10.1109/TCAD.2018.2858464">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Chou18b&#39;,&#39;bibtex&#39;)">Cite</a>] <br>
                <b><span style="color:red">Also presented at 2018 University of Michigan Engineering Graduate Symposium; <i>won Emerging Research Social Impact award</i>.</span></b>   </td>
</tr>
<tr id="abs_Chou18b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: This paper employs correct-by-construction control synthesis, in particular controlled invariant set computations, for falsification. Our hypothesis is that if it is possible to compute a “large enough" controlled invariant set either for the actual system model or some simplification of the system model, interesting corner cases for other control designs can be generated by sampling initial conditions from the boundary of this controlled invariant set. Moreover, if falsifying trajectories for a given control design can be found through such sampling, then the controlled invariant set can be used as a supervisor to ensure safe operation of the control design under consideration. In addition to interesting initial conditions, which are mostly related to safety violations in transients, we use solutions from a dual game, a reachability game for the safety specification, to find falsifying inputs. We also propose optimization-based heuristics for input generation for cases when the state is outside the winning set of the dual game. To demonstrate the proposed ideas, we consider case studies from basic autonomous driving functionality, in particular, adaptive cruise control and lane keeping. We show how the proposed technique can be used to find interesting falsifying trajectories for classical control designs like proportional controllers, proportional integral controllers and model predictive controllers, as well as an open source real-world autonomous driving package. </div></td>
  </tr>
<tr id="bib_Chou18b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@article{Chou-et-al-Journal-18,<br>   Author = "Glen Chou, Yunus E. Sahin, Liren Yang, Kwesi J. Rutledge, and Necmiye Ozay",
   journal = {IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (ESWEEK-TCAD special issue)},<br>   Title = "Using control synthesis to generate corner cases: A case study on autonomous driving",<br>   year = {2018}<br>}</pre></td>
</tr>
<tr id="notes_Chou18b" class="notes noshow">
    <td colspan="3"><div align="justify"> <b><span style="color:red">Notes</span></b>: Also presented at 2018 University of Michigan Engineering Graduate Symposium; <i>won Emerging Research Social Impact award</i>. </div></td>
  </tr>


</tbody>
</table>
<!-- <hr> -->

<br>

## Peer-Reviewed Conference Papers

<hr>

<table class="table">
<colgroup>
	<col width="27%" />
	<col width="2%" />
	<col width="71%" />
</colgroup>
<tbody>


<tr id="Lin24">
	<td markdown="span"><br><img src="../images/icra_24_01.png" onmouseover="this.src='../images/icra_24_02.png'" onmouseout="this.src='../images/icra_24_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Improving Out-of-Distribution Generalization of Learned Dynamics by Learning Pseudometrics and Constraint Manifolds** <br> 
		<em>Yating Lin, **Glen Chou**, Dmitry Berenson</em> <br> 
		Proceedings of the 61st IEEE International Conference on Robotics and Automation (ICRA), May 2024. <br>
		[<a href="javascript:toggleInfo(&#39;Lin24&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Lin24&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2403.12245)\] \[<a href="https://arxiv.org/pdf/2403.12245">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Lin24&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Lin24" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We propose a method for improving the prediction accuracy of learned robot dynamics models on out-of-distribution (OOD) states. We achieve this by leveraging two key sources of structure often present in robot dynamics: 1) sparsity, i.e., some components of the state may not affect the dynamics, and 2) physical limits on the set of possible motions, in the form of nonholonomic constraints. Crucially, we do not assume this structure is known a priori, and instead learn it from data. We use contrastive learning to obtain a distance pseudometric that uncovers the sparsity pattern in the dynamics, and use it to reduce the input space when learning the dynamics. We then learn the unknown constraint manifold by approximating the normal space of possible motions from the data, which we use to train a Gaussian process (GP) representation of the constraint manifold. We evaluate our approach on a physical differential-drive robot and a simulated quadrotor, showing improved prediction accuracy on OOD data relative to baselines. </div></td>
  </tr>
<tr id="bib_Lin24" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Lin-ICRA-24,<br>   Author = "Yating Lin, Glen Chou, Dmitry Berenson",
   journal = {Proceedings of the 61st IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "Improving Out-of-Distribution Generalization of Learned Dynamics by Learning Pseudometrics and Constraint Manifolds",<br>   year = {2024}<br>}</pre></td>
</tr>

<tr id="Chou23a">
	<td markdown="span"><br><img src="../images/cdc_23_01.png" onmouseover="this.src='../images/cdc_23_02.gif'" onmouseout="this.src='../images/cdc_23_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Synthesizing Stable Reduced-Order Visuomotor Policies for Nonlinear Systems via Sums-of-Squares Optimization** <br> 
		<em>**Glen Chou**, Russ Tedrake</em> <br> 
		Proceedings of the 62nd IEEE Conference on Decision and Control (CDC), December 2023. <br>
		[<a href="javascript:toggleInfo(&#39;Chou23a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou23a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2304.12405)\] \[<a href="https://glenchou.github.io/papers/Chou23a.pdf">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Chou23a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou23a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for synthesizing dynamic, reduced-order output-feedback polynomial control policies for control-affine nonlinear systems which guarantees runtime stability to a goal state, when using visual observations and a learned perception module in the feedback control loop. We leverage Lyapunov analysis to formulate the problem of synthesizing such policies. This problem is nonconvex in the policy parameters and the Lyapunov function that is used to prove the stability of the policy. To solve this problem approximately, we propose two approaches: the first solves a sequence of sum-of-squares optimization problems to iteratively improve a policy which is provably-stable by construction, while the second directly performs gradient-based optimization on the parameters of the polynomial policy, and its closed-loop stability is verified a posteriori. We extend our approach to provide stability guarantees in the presence of observation noise, which realistically arises due to errors in the learned perception module. We evaluate our approach on several underactuated nonlinear systems, including pendula and quadrotors, showing that our guarantees translate to empirical stability when controlling these systems from images, while baseline approaches can fail to reliably stabilize the system. </div></td>
  </tr>
<tr id="bib_Chou23a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-CDC-23,<br>   Author = "Glen Chou and Russ Tedrake",
   journal = {Proceedings of the 62nd IEEE Conference on Decision and Control (CDC)},<br>   Title = "Synthesizing Stable Reduced-Order Visuomotor Policies for Nonlinear Systems via Sums-of-Squares Optimization",<br>   year = {2023}<br>}</pre></td>
</tr>

<tr id="Suh23">
	<td markdown="span"><br><img src="../images/corl_23_01.png" onmouseover="this.src='../images/corl_23_02.gif'" onmouseout="this.src='../images/corl_23_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Fighting Uncertainty with Gradients: Offline Reinforcement Learning via Diffusion Score Matching** <br> 
		<em>H.J. Terry Suh, **Glen Chou\***, Hongkai Dai\*, Lujie Yang\*, Abhishek Gupta, Russ Tedrake</em> <br> 
		7th Conference on Robot Learning (CoRL), November 2023. <br>
		[<a href="javascript:toggleInfo(&#39;Suh23&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Suh23&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2306.14079)\] \[<a href="https://arxiv.org/pdf/2306.14079.pdf">PDF</a>\] \[<a href="https://youtu.be/rNpHt3rNkJo">Supplementary Video</a>\] \[<a href="https://github.com/hjsuh94/score_po">Code</a>\] \[<a href="https://sites.google.com/view/score-guided-planning/home">Website</a>\] [<a href="javascript:toggleInfo(&#39;Suh23&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Suh23" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Offline optimization paradigms such as offline Reinforcement Learning (RL) or Imitation Learning (IL) allow policy search algorithms to make use of offline data, but require careful incorporation of uncertainty in order to circumvent the challenges of distribution shift. Gradient-based policy search methods are a promising direction due to their effectiveness in high dimensions; however, we require a more careful consideration of how these methods interplay with uncertainty estimation. We claim that in order for an uncertainty metric to be amenable for gradient-based optimization, it must be (i) stably convergent to data when uncertainty is minimized with gradients, and (ii) not prone to underestimation of true uncertainty. We investigate smoothed distance to data as a metric, and show that it not only stably converges to data, but also allows us to analyze model bias with Lipschitz constants. Moreover, we establish an equivalence between smoothed distance to data and data likelihood, which allows us to use score-matching techniques to learn gradients of distance to data. Importantly, we show that offline model-based policy search problems that maximize data likelihood do not require values of likelihood; but rather only the gradient of the log likelihood (the score function). Using this insight, we propose Score-Guided Planning (SGP), a planning algorithm for offline RL that utilizes score-matching to enable first-order planning in high-dimensional problems, where zeroth-order methods were unable to scale, and ensembles were unable to overcome local minima. </div></td>
  </tr>
<tr id="bib_Suh23" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Suh-CoRL-23,<br>   Author = "HJ Terry Suh, Glen Chou, Hongkai Dai, Lujie Yang, Abhishek Gupta, and Russ Tedrake",
   journal = {7th Conference on Robot Learning (CoRL)},<br>   Title = "Fighting Uncertainty with Gradients: Offline Reinforcement Learning via Diffusion Score Matching",<br>   year = {2023}<br>}</pre></td>
</tr>

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
	<td markdown="span"><br><img src="../images/cdc_21_01.png" onmouseover="this.src='../images/cdc_21_02.png'" onmouseout="this.src='../images/cdc_21_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Model Error Propagation via Learned Contraction Metrics for Safe Feedback Motion Planning of Unknown Systems** <br> 
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

<tr id="Rutledge21a">
	<td markdown="span"><br><img src="../images/hscc_21_01.png" onmouseover="this.src='../images/hscc_21_02.gif'" onmouseout="this.src='../images/hscc_21_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Compositional Safety Rules for Inter-Triggering Hybrid Automata** <br> 
		<em>Kwesi J. Rutledge\*, **Glen Chou\***, Necmiye Ozay</em> <br> 
		Proceedings of the 24th International Conference on Hybrid Systems: Computation and Control (HSCC), May 2021. <br>
		[<a href="javascript:toggleInfo(&#39;Rutledge21a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Rutledge21a&#39;); ">Abstract</a>]
                \[[PDF](https://deepblue.lib.umich.edu/bitstream/handle/2027.42/166479/The_Inter_Triggering_Hybrid_Automaton.pdf)\] \[<a href="https://doi.org/10.1145/3447928.3456659">DOI</a>\] \[<a href="https://youtu.be/a5IULWQYVzM">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Rutledge21a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Rutledge21a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: In this paper, we present a compositional condition for ensuring safety of a collection of interacting systems modeled by inter-triggering hybrid automata (ITHA). ITHA is a modeling formalism for representing multi-agent systems in which each agent is governed by individual dynamics but can also interact with other agents through triggering actions. These triggering actions result in a jump/reset in the state of other agents according to a global resolution function. A sufficient condition for safety of the collection, inspired by responsibility-sensitive safety, is developed in two parts: self-safety relating to the individual dynamics, and responsibility relating to the triggering actions. The condition relies on having an over-approximation method for the resolution function. We further show how such over-approximations can be obtained and improved via communication. We use two examples, a job scheduling task on parallel processors and a highway driving example, throughout the paper to illustrate the concepts. Finally, we provide a comprehensive evaluation on how the proposed condition can be leveraged for several multi-agent control and supervision examples. </div></td>
  </tr>
<tr id="bib_Rutledge21a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Rutledge-HSCC-21,<br>   Author = "Kwesi Rutledge, Glen Chou, and Necmiye Ozay",
   journal = {Proceedings of the 24th International Conference on Hybrid Systems: Computation and Control (HSCC)},<br>   Title = "Compositional Safety Rules for Inter-Triggering Hybrid Automata",<br>   year = {2021}<br>}</pre></td>
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

<tr id="Chou20b">
	<td markdown="span"><br><img src="../images/rss_20_01.png" onmouseover="this.src='../images/rss_20_02.gif'" onmouseout="this.src='../images/rss_20_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Explaining Multi-stage Tasks by Learning Temporal Logic Formulas from Suboptimal Demonstrations** <br>
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of Robotics: Science and Systems (RSS) XVI, July 2020. <br>
	 [<a href="javascript:toggleInfo(&#39;Chou20b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou20b&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2006.02411)\] \[<a href="https://doi.org/10.15607/RSS.2020.XVI.097">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=8DPtL1-KeoM">Talk</a>\] \[<a href="https://www.youtube.com/watch?v=cpUEcWCUMqc">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Chou20b&#39;,&#39;bibtex&#39;)">Cite</a>] <br>
         <b><span style="color:red">Invited to AURO special issue.</span></b>   </td>
</tr>
<tr id="abs_Chou20b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for learning multi-stage tasks from demonstrations by learning the logical structure and atomic propositions of a consistent linear temporal logic (LTL) formula. The learner is given successful but potentially suboptimal demonstrations, where the demonstrator is optimizing a cost function while satisfying the LTL formula, and the cost function is uncertain to the learner. Our algorithm uses the Karush-Kuhn-Tucker (KKT) optimality conditions of the demonstrations together with a counterexample-guided falsification strategy to learn the atomic proposition parameters and logical structure of the LTL formula, respectively. We provide theoretical guarantees on the conservativeness of the recovered atomic proposition sets, as well as completeness in the search for finding an LTL formula consistent with the demonstrations. We evaluate our method on high-dimensional nonlinear systems by learning LTL formulas explaining multi-stage tasks on 7-DOF arm and quadrotor systems and show that it outperforms competing methods for learning LTL formulas from positive examples. </div></td>
  </tr>
<tr id="bib_Chou20b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-RSS-20,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of Robotics: Science and Systems (RSS) XVI},<br>   Title = "Explaining Multi-stage Tasks by Learning Temporal Logic Formulas from Suboptimal Demonstrations",<br>   year = {2020}<br>}</pre></td>
</tr>

<tr id="Knuth20a">
	<td markdown="span"><br><img src="../images/wafr_20_01.png" onmouseover="this.src='../images/wafr_20_02.png'" onmouseout="this.src='../images/wafr_20_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Inferring Obstacles and Path Validity from Visibility-Constrained Demonstrations** <br> 
		<em>Craig Knuth, **Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of the 14th International Workshop on the Algorithmic Foundations of Robotics (WAFR), June 2020. <br>
		[<a href="javascript:toggleInfo(&#39;Knuth20a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Knuth20a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2005.05421)\] \[<a href="https://doi.org/10.1007/978-3-030-66723-8_2">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Knuth20a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Knuth20a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Many methods in learning from demonstration assume that the demonstrator has knowledge of the full environment. However, in many scenarios, a demonstrator only sees part of the environment and they continuously replan as they gather information. To plan new paths or to reconstruct the environment, we must consider the visibility constraints and replanning process of the demonstrator, which, to our knowledge, has not been done in previous work. We consider the problem of inferring obstacle configurations in a 2D environment from demonstrated paths for a point robot that is capable of seeing in any direction but not through obstacles. Given a set of \textit{survey points}, which describe where the demonstrator obtains new information, and a candidate path, we construct a Constraint Satisfaction Problem (CSP) on a cell decomposition of the environment. We parameterize a set of obstacles corresponding to an assignment from the CSP and sample from the set to find valid environments. We show that there is a probabilistically-complete, yet not entirely tractable, algorithm that can guarantee novel paths in the space are unsafe or possibly safe. We also present an incomplete, but empirically-successful, heuristic-guided algorithm that we apply in our experiments to 1) planning novel paths and 2) recovering a probabilistic representation of the environment. </div></td>
  </tr>
<tr id="bib_Knuth20a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Knuth-WAFR-20,<br>   Author = "Craig Knuth, Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of the 14th International Workshop on the Algorithmic Foundations of Robotics (WAFR)},<br>   Title = "Inferring Obstacles and Path Validity from Visibility-Constrained Demonstrations",<br>   year = {2020}<br>}</pre></td>
</tr>

<tr id="Chou19b">
	<td markdown="span"><br><img src="../images/corl_19_01.png" onmouseover="this.src='../images/corl_19_02.png'" onmouseout="this.src='../images/corl_19_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Parametric Constraints in High Dimensions from Demonstrations** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of the 3rd Conference on Robot Learning (CoRL), November 2019. <br>
		[<a href="javascript:toggleInfo(&#39;Chou19b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou19b&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/1910.03477)\] \[<a href="http://proceedings.mlr.press/v100/chou20a.html">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Chou19b&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou19b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a scalable algorithm for learning parametric constraints in high dimensions from safe expert demonstrations. To reduce the ill-posedness of the constraint recovery problem, our method uses hit-and-run sampling to generate lower cost, and thus unsafe, trajectories. Both safe and unsafe trajectories are used to obtain a representation of the unsafe set that is compatible with the data by solving an integer program in that representation's parameter space. Our method can either leverage a known parameterization or incrementally grow a parameterization while remaining consistent with the data, and we provide theoretical guarantees on the conservativeness of the recovered unsafe set. We evaluate our method on high-dimensional constraints for high-dimensional systems by learning constraints for 7-DOF arm, quadrotor, and planar pushing examples, and show that our method outperforms baseline approaches. </div></td>
  </tr>
<tr id="bib_Chou19b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-CoRL-19,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of the 3rd Conference on Robot Learning (CoRL)},<br>   Title = "Learning Parametric Constraints in High Dimensions from Demonstration",<br>   year = {2019}<br>}</pre></td>
</tr>



<tr id="Chou18d">
	<td markdown="span"><br><img src="../images/wafr_18_01.png" onmouseover="this.src='../images/wafr_18_02.png'" onmouseout="this.src='../images/wafr_18_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Constraints from Demonstrations** <br> 
		<em>**Glen Chou**, Dmitry Berenson, Necmiye Ozay</em> <br> 
		Proceedings of the 14th International Workshop on the Algorithmic Foundations of Robotics (WAFR), December 2018. <br>
		[<a href="javascript:toggleInfo(&#39;Chou18d&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou18d&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/1812.07084)\] \[<a href="https://doi.org/10.1007/978-3-030-44051-0_14">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Chou18d&#39;,&#39;bibtex&#39;)">Cite</a>] <br>
         <b><span style="color:red">Invited to IJRR special issue.</span></b>   </td>
</tr>
<tr id="abs_Chou18d" class="abstract noshow">
    <td colspan="4"><div align="justify"> <b>Abstract</b>: We extend the learning from demonstration paradigm by providing a method for learning unknown constraints shared across tasks, using demonstrations of the tasks, their cost functions, and knowledge of the system dynamics and control constraints. Given safe demonstrations, our method uses hit-and-run sampling to obtain lower cost, and thus unsafe, trajectories. Both safe and unsafe trajectories are used to obtain a consistent representation of the unsafe set via solving an integer program. Our method generalizes across system dynamics and learns a guaranteed subset of the constraint. We also provide theoretical analysis on what subset of the constraint can be learnable from safe demonstrations. We demonstrate our method on linear and nonlinear system dynamics, show that it can be modi ed to work with suboptimal demonstrations, and that it can also be used to solve a transfer learning task. </div></td>
  </tr>
<tr id="bib_Chou18d" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-WAFR-18,<br>   Author = "Glen Chou, Dmitry Berenson, and Necmiye Ozay",
   journal = {Proceedings of the 13th International Workshop on the Algorithmic Foundations of Robotics (WAFR)},<br>   Title = "Learning Constraints from Demonstration",<br>   year = {2018}<br>}</pre></td>
</tr>



<tr id='Chou18c'>
	<td markdown="span"><br><img src="../images/emsoft_18_01.png" onmouseover="this.src='../images/emsoft_18_02.png'" onmouseout="this.src='../images/emsoft_18_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Using control synthesis to generate corner cases: A case study on autonomous driving** <br> 
		<em>**Glen Chou**\*, Yunus E. Sahin\*, Liren Yang\*, Kwesi J. Rutledge, Petter Nilsson, Necmiye Ozay</em> <br> 
		Proceedings of the ACM SIGBED International Conference on Embedded Software (EMSOFT), October 2018. <br>
		[<a href="javascript:toggleInfo(&#39;Chou18c&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou18c&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/1807.09537)\] \[<a href="https://doi.org/10.1109/TCAD.2018.2858464">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Chou18c&#39;,&#39;bibtex&#39;)">Cite</a>] <br>
                <b><span style="color:red">Also presented at 2018 University of Michigan Engineering Graduate Symposium; <i>won Emerging Research Social Impact award</i>.</span></b>   </td>
</tr>
<tr id="abs_Chou18c" class="abstract noshow">
    <td colspan="4"><div align="justify"> <b>Abstract</b>: This paper employs correct-by-construction control synthesis, in particular controlled invariant set computations, for falsification. Our hypothesis is that if it is possible to compute a “large enough" controlled invariant set either for the actual system model or some simplification of the system model, interesting corner cases for other control designs can be generated by sampling initial conditions from the boundary of this controlled invariant set. Moreover, if falsifying trajectories for a given control design can be found through such sampling, then the controlled invariant set can be used as a supervisor to ensure safe operation of the control design under consideration. In addition to interesting initial conditions, which are mostly related to safety violations in transients, we use solutions from a dual game, a reachability game for the safety specification, to find falsifying inputs. We also propose optimization-based heuristics for input generation for cases when the state is outside the winning set of the dual game. To demonstrate the proposed ideas, we consider case studies from basic autonomous driving functionality, in particular, adaptive cruise control and lane keeping. We show how the proposed technique can be used to find interesting falsifying trajectories for classical control designs like proportional controllers, proportional integral controllers and model predictive controllers, as well as an open source real-world autonomous driving package. </div></td>
  </tr>
<tr id="bib_Chou18c" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-et-al-EMSOFT-18,<br>   Author = "Glen Chou, Yunus E. Sahin, Liren Yang, Kwesi J. Rutledge, and Necmiye Ozay",
   journal = {Proceedings of the ACM SIGBED International Conference on Embedded Software (EMSOFT)},<br>   Title = "Using control synthesis to generate corner cases: A case study on autonomous driving",<br>   year = {2018}<br>}</pre></td>
</tr>



<tr id='Chou18a'>
	<td markdown="span"><br><img src="../images/sysid_18_01.png" onmouseover="this.src='../images/sysid_18_02.png'" onmouseout="this.src='../images/sysid_18_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Incremental Segmentation of ARX Models** <br> 
		<em>**Glen Chou**, Necmiye Ozay, Dmitry Berenson</em> <br> 
		Proceedings of the 18th IFAC Symposium on System Identification (SYSID), July 2018. <br>
		[<a href="javascript:toggleInfo(&#39;Chou18a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou18a&#39;); ">Abstract</a>]
                \[<a href="https://glenchou.github.io/papers/Chou18a.pdf">PDF</a>\] \[<a href="https://doi.org/10.1016/j.ifacol.2018.09.222">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Chou18a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou18a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We consider the problem of incrementally segmenting auto-regressive models with exogenous inputs (ARX models) when the data is received sequentially at run-time. In particular, we extend a recently proposed dynamic programming based polynomial-time algorithm for offline (batch) ARX model segmentation to the incremental setting. The new algorithm enables sequential updating of the models, eliminating repeated computation, while remaining optimal. We also show how certain noise bounds can be used to detect switches automatically at run-time. The efficiency of the approach compared to the batch method is illustrated on synthetic and real data. </div></td>
  </tr>
<tr id="bib_Chou18a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-SYSID-18,<br>   Author = "Glen Chou, Necmiye Ozay, and Dmitry Berenson",
   journal = {Proceedings of the 18th IFAC Symposium on System Identification (SYSID)},<br>   Title = "Incremental Segmentation of ARX Models",<br>   year = {2018}<br>}</pre></td>
</tr>



<tr id='Dhinakaran17'>
	<td markdown="span"><br><img src="../images/cdc_17_01.png" onmouseover="this.src='../images/cdc_17_02.png'" onmouseout="this.src='../images/cdc_17_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**A Hybrid Framework for Multi-Vehicle Collision Avoidance** <br>
		<em>Aparna Dhinakaran\*, Mo Chen\*, **Glen Chou**, Jennifer C. Shih, Claire J. Tomlin</em> <br> 
		Proceedings of the 56th IEEE Conference on Decision and Control (CDC), December 2017. <br>
		[<a href="javascript:toggleInfo(&#39;Dhinakaran17&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Dhinakaran17&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/1703.07375)\] \[<a href="https://doi.org/10.1109/CDC.2017.8264092">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Dhinakaran17&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Dhinakaran17" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: With the recent surge of interest in UAVs for civilian services, the importance of developing tractable multi-agent analysis techniques that provide safety and performance guarantees have drastically increased. Hamilton-Jacobi (HJ) reachability has successfully provided these guarantees to small-scale systems and is flexible in terms of system dynamics. However, the exponential complexity scaling of HJ reachability with respect to system dimension prevents its direct application to larger-scale problems where the number of vehicles is greater than two. In this paper, we propose a collision avoidance algorithm using a hybrid framework for N+1 vehicles through higher-level control logic given any N-vehicle collision avoidance algorithm. Our algorithm conservatively approximates a guaranteed-safe region in the joint state space of the N+1 vehicles and produces a safety-preserving controller. In addition, our algorithm does not incur significant additional computation cost. We demonstrate our proposed method in simulation. </div></td>
  </tr>
<tr id="bib_Dhinakaran17" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Dhinakaran-et-al-CDC-17,
  	author    = {Aparna Dhinakaran and
               Mo Chen and
               Glen Chou and
               Jennifer C. Shih and
               Claire J. Tomlin},
  title     = {A hybrid framework for multi-vehicle collision avoidance},
  booktitle = {56th {IEEE} Annual Conference on Decision and Control, {CDC} 2017,
               Melbourne, Australia, December 12-15, 2017},
  pages     = {2979--2984},
  year      = {2017},<br>}</pre></td>
</tr>


</tbody>
</table>
<!-- <hr> -->

<br>

## Refereed Workshop Papers/Technical Reports

<hr>

<br />

<table class="table">
<colgroup>
	<col width="27%" />
	<col width="2%" />
	<col width="71%" />
</colgroup>
<tbody>

<tr id="Chou22c">
	<td markdown="span"><br><img src="../images/rsspw_01.png" onmouseover="this.src='../images/rsspw_01.png'" onmouseout="this.src='../images/rsspw_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Safely Integrating Perception, Planning, and Control for Robust Learning-Based Robot Autonomy** <br> 
		<em>**Glen Chou\***</em> <br> 
		Robotics: Science and Systems, Pioneers Workshop, June 2022. <br>
                \[[PDF](https://glenchou.github.io/papers/Chou22c.pdf)\] [<a href="javascript:toggleInfo(&#39;Chou22c&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="bib_Chou22c" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-RSSPioneersWS-22,<br>   Author = "Glen Chou",
   journal = {Robotics: Science and Systems, Pioneers Workshop},<br>   Title = "Safely Integrating Perception, Planning, and Control for Robust Learning-Based Robot Autonomy",<br>   year = {2022}<br>}</pre></td>
</tr>

<tr id="Wang21a">
	<td markdown="span"><br><img src="../images/ral_22_01.jpg" onmouseover="this.src='../images/ral_22_02.gif'" onmouseout="this.src='../images/ral_22_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Gaussian Process Constraint Learning for Scalable Safe Motion Planning from Demonstrations** <br> 
		<em>Hao Wang\*, **Glen Chou\***, Dmitry Berenson</em> <br> 
		Robotics: Science and Systems, Workshop on Integrating Planning and Learning, July 2021. <br>
		[<a href="javascript:toggleInfo(&#39;Wang21a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstract/Wang21a&#39;); ">Abstract</a>]
                \[[PDF](https://glenchou.github.io/papers/Wang21a.pdf)\] [<a href="javascript:toggleInfo(&#39;Wang21a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Wang21a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We propose a method for learning constraints represented as Gaussian processes (GPs) from locally-optimal demonstrations. Our approach uses the Karush-Kuhn-Tucker (KKT) optimality conditions of the demonstrations to determine the location and shape of the constraints, and uses these to train a GP which is consistent with this information. We demonstrate our method on a 12D quadrotor constraint learning problem, showing that the learned constraint is accurate and can be used within a kinodynamic RRT to plan probabilistically-safe trajectories. </div></td>
  </tr>
<tr id="bib_Wang21a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Wang-RSSWS-21,<br>   Author = "Hao Wang, Glen Chou, and Dmitry Berenson",
   journal = {Robotics: Science and Systems, Workshop on Integrating Planning and Learning},<br>   Title = "Gaussian Process Constraint Learning for Scalable Safe Motion Planning from Demonstrations",<br>   year = {2021}<br>}</pre></td>
</tr>

<tr id="Chou19a">
	<td markdown="span"><br><img src="../images/corl_19_01.png" onmouseover="this.src='../images/corl_19_02.png'" onmouseout="this.src='../images/corl_19_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Parametric Constraints in High Dimensions from Demonstrations** <br> 
		<em>**Glen Chou**, Dmitry Berenson, Necmiye Ozay</em> <br> 
		Robotics: Science and Systems, Workshop on Robust Autonomy, June 2019. <br>
		[<a href="javascript:toggleInfo(&#39;Chou19a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstract/Chou19a&#39;); ">Abstract</a>]
                \[[PDF](https://openreview.net/pdf?id=SJxqVK-opV)\] [<a href="javascript:toggleInfo(&#39;Chou19a&#39;,&#39;bibtex&#39;)">Cite</a>] <br>
         <b><span style="color:red">Selected for long contributed talk.</span></b>   </td>
</tr>
<tr id="abs_Chou19a" class="abstract noshow">
    <td colspan="4"><div align="justify"> <b>Abstract</b>: We extend the learning from demonstration paradigm by providing a method for learning unknown constraints shared across tasks, using demonstrations of the tasks, their cost functions, and knowledge of the system dynamics and control constraints. Given safe demonstrations, our method uses hit-and-run sampling to obtain lower cost, and thus unsafe, trajectories. Both safe and unsafe trajectories are used to obtain a consistent representation of the unsafe set via solving a mixed integer program. Additionally, by leveraging a known parameterization of the constraint, we modify our method to learn parametric constraints in high dimensions. We show that our method can learn a six-dimensional pose constraint for a 7-DOF robot arm. </div></td>
  </tr>
<tr id="bib_Chou19a" class="bibtex noshow">
<td colspan="4"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-RSSWS-19,<br>   Author = "Glen Chou, Dmitry Berenson, and Necmiye Ozay",
   journal = {Robotics: Science and Systems, Workshop on Robust Autonomy},<br>   Title = "Learning Parametric Constraints in High Dimensions from Demonstration",<br>   year = {2019}<br>}</pre></td>
</tr>


<tr id='Jiang16'>
	<td markdown="span"><br><img src="../images/arxiv_16_01.png" onmouseover="this.src='../images/arxiv_16_02.png'" onmouseout="this.src='../images/arxiv_16_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Using neural networks to compute approximate and guaranteed feasible Hamilton-Jacobi-Bellman PDE solutions** <br>
		<em>Frank Jiang\*, **Glen Chou**\*, Mo Chen\*, Claire J. Tomlin </em> <br> 
		arXiv, November 2016. <br>
		[<a href="javascript:toggleInfo(&#39;Jiang16&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Jiang16&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/1611.03158)\] [<a href="javascript:toggleInfo(&#39;Jiang16&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Jiang16" class="abstract noshow">
    <td colspan="4"><div align="justify"> <b>Abstract</b>: To sidestep the curse of dimensionality when computing solutions to Hamilton-Jacobi-Bellman partial differential equations (HJB PDE), we propose an algorithm that leverages a neural network to approximate the value function. We show that our final approximation of the value function generates near optimal controls which are guaranteed to successfully drive the system to a target state. Our framework is not dependent on state space discretization, leading to a significant reduction in computation time and space complexity in comparison with dynamic programming-based approaches. Using this grid-free approach also enables us to plan over longer time horizons with relatively little additional computation overhead. Unlike many previous neural network HJB PDE approximating formulations, our approximation is strictly conservative and hence any trajectories we generate will be strictly feasible. For demonstration, we specialize our new general framework to the Dubins car model and discuss how the framework can be applied to other models with higher-dimensional state spaces. </div></td>
  </tr>
<tr id="bib_Jiang16" class="bibtex noshow">
<td colspan="4"><b>BibTeX</b>:
  <pre>@inproceedings{Jiang-et-al-16,
  	author    = {Frank J. Jiang and
               Glen Chou and
               Mo Chen and
               Claire J. Tomlin},
  title     = {Using neural networks to compute approximate and guaranteed feasible Hamilton-Jacobi-Bellman PDE solutions},
  journal   = {CoRR},
  volume    = {abs/1611.03158},
  year      = {2016},<br>}</pre></td>
</tr>


</tbody>
</table>
<hr>
