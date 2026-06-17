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
	<col width="18%" />
	<col width="2%" />
	<col width="80%" />
</colgroup>
<tbody>
<style>
  table.table {
    font-size: 0.95em;
  }
  table.table td {
    padding-top: 0.0rem;
    padding-bottom: 0.6rem;
    line-height: 1.2;
    vertical-align: middle;
  }
  table.table > tbody > tr:nth-child(odd):not(.abstract):not(.bibtex):not(.notes) {
    background: #ffffff;
  }

  table.table > tbody > tr:nth-child(even):not(.abstract):not(.bibtex):not(.notes) {
    background: #f5f5f5;
  }
</style>

<tr id="Hong26a">
	<td markdown="span"><br><img src="../images/ral_26_polymerge.jpg" onmouseover="this.src='../images/ral_26_polymerge.gif'" onmouseout="this.src='../images/ral_26_polymerge.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**PolyMerge: Compressing 3D Gaussian Splats with Polytope Coverings for Provably Safe Resource-Constrained Navigation** <br> 
		<em>Jihoon Hong, Chih-Yuan Chiu, Sara Fridovich-Keil, **Glen Chou**</em> <br> 
		IEEE Robotics and Automation Letters (RA-L), with presentation at IROS 2026, vol. 11, no. 7, pp. 8512-8519, July 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Hong26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Hong26a&#39;); ">Abstract</a>]
                 \[[arXiv](https://arxiv.org/abs/2606.16232)\] \[[PDF](https://arxiv.org/pdf/2606.16232)\] \[<a href="https://doi.org/10.1109/LRA.2026.3692083">DOI</a>\] \[<a href="https://athlon76.github.io/PolyMerge-website/">Project Website</a>\] \[<a href="https://www.youtube.com/watch?v=eEdih0tga0M">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Hong26a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Hong26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Obstacle avoidance is essential for safe navigation and motion planning. Recent advances in radiance field reconstruction have enabled object detection and modeling with unprecedented fidelity, but remain too memory- and compute-intensive for deployment in on-board perception-based motion planning. To address these limitations, we propose PolyMerge to transform a large, photorealistic 3D Gaussian Splatting (3DGS) model of a scene into a lightweight representation as a set of convex polytopes whose enclosed volume is guaranteed to over-approximate all obstacles in the original 3DGS model. PolyMerge uses a variable number of polytopes to trade off conservativeness and computational cost, and integrates with polytope-based control barrier functions (CBFs) to ensure collision-free path planning. We showcase PolyMerge in simulation and hardware experiments using a small Crazyflie drone, which uses PolyMerge to compute and follow safe trajectories in real time using extremely limited onboard compute resources, outperforming baselines in speed while guaranteeing safety. </div></td>
  </tr>
  <tr id="bib_Hong26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Hong-RAL-26,<br>   Author = "Jihoon Hong, Chih-Yuan Chiu, Sara Fridovich-Keil, and Glen Chou",
   journal = {IEEE Robotics and Automation Letters (RA-L)},<br>   Title = "PolyMerge: Compressing 3D Gaussian Splats with Polytope Coverings for Provably Safe Resource-Constrained Navigation",<br>   year = {2026}<br>}</pre></td>
</tr>


<tr id="Zhang26a">
	<td markdown="span"><br><img src="../images/ral26_multicl.jpg" onmouseover="this.src='../images/ral26_multicl.gif'" onmouseout="this.src='../images/ral26_multicl.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Constraint Learning in Multi-Agent Dynamic Games from Demonstrations of Local Nash Interactions** <br> 
		<em>Zhouyu Zhang\*, Chih-Yuan Chiu\*, **Glen Chou**</em> <br> 
		IEEE Robotics and Automation Letters (RA-L), with presentation at IROS 2026, vol. 11, no. 6, pp. 6696-6703, March 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Zhang26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Zhang26a&#39;); ">Abstract</a>]
                 \[[arXiv](https://arxiv.org/abs/2508.19945)\] \[[PDF](https://ieeexplore.ieee.org/document/11455925)\] \[<a href="https://doi.org/10.1109/LRA.2026.3677745">DOI</a>\] \[<a href="https://www.youtube.com/watch?v=62HpDQlrQiI">Supplementary Video</a>\] [<a href="javascript:toggleInfo(&#39;Zhang26a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Zhang26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present an inverse dynamic game-based algorithm to learn parametric constraints from a given dataset of local Nash equilibrium interactions between multiple agents. Specifically, we introduce mixed-integer linear programs (MILP) encoding the Karush-Kuhn-Tucker (KKT) conditions of the interacting agents, which recover constraints consistent with the local Nash stationarity of the interaction demonstrations. We establish theoretical guarantees that our method learns inner approximations of the true safe and unsafe sets. We also use the interaction constraints recovered by our method to design motion plans that robustly satisfy the underlying constraints. Across simulations and hardware experiments, our methods accurately inferred constraints and designed safe interactive motion plans for various classes of constraints, both convex and non-convex, from interaction demonstrations of agents with nonlinear dynamics. </div></td>
  </tr>
  <tr id="bib_Zhang26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Zhang-RAL-26,<br>   Author = "Zhouyu Zhang, Chih-Yuan Chiu, and Glen Chou",
   journal = {IEEE Robotics and Automation Letters (RA-L)},<br>   Title = "Constraint Learning in Multi-Agent Dynamic Games from Demonstrations of Local Nash Interactions",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Chiu26a">
	<td markdown="span"><br><img src="../images/lcss26_01.png" onmouseover="this.src='../images/lcss26_01.png'" onmouseout="this.src='../images/lcss26_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Learning Constraints from Stochastic Partially-Observed Closed-Loop Demonstrations** <br> 
		<em>Chih-Yuan Chiu\*, Zhouyu Zhang\*, **Glen Chou**</em> <br> 
		IEEE Control Systems Letters (L-CSS), with presentation at ACC 2026, vol. 10, pp. 43-48, January 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Chiu26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chiu26a&#39;); ">Abstract</a>]
                 \[[arXiv](https://arxiv.org/abs/2509.15109)\] \[[PDF](https://ieeexplore.ieee.org/abstract/document/11363606)\] \[<a href="https://doi.org/10.1109/LCSYS.2026.3657991">DOI</a>\] [<a href="javascript:toggleInfo(&#39;Chiu26a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chiu26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for learning unknown parametric constraints from locally-optimal input-output trajectory data. We assume the data is generated by rollouts of stochastic nonlinear dynamics, under a single state or output feedback law and initial condition but distinct noise realizations, to robustly satisfy underlying constraints despite worst-case noise outcomes. We encode the Karush-Kuhn-Tucker (KKT) conditions of this robust optimal feedback control problem within a feasibility problem to recover constraints consistent with the local optimality of the demonstrations. We prove that our constraint learning method (i) accurately recovers the demonstrator’s policy, and (ii) conservatively estimates the set of policies that ensure constraint satisfaction despite worst-case noise realizations. Moreover, we perform sensitivity analysis, proving that when demonstrations are corrupted by transmission error, the inaccuracy in the learned feedback law scales linearly in the error magnitude. Empirically, our method accurately recovers unknown constraints from simulated noisy, closed-loop demonstrations generated using dynamics, both linear and nonlinear, (e.g., unicycle and quadrotor) and a range of feedback mechanisms. </div></td>
  </tr>
  <tr id="bib_Chiu26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chiu-LCSS-26,<br>   Author = "Zhouyu Zhang, Chih-Yuan Chiu, and Glen Chou",
   journal = {IEEE Control Systems Letters (L-CSS)},<br>   Title = "Learning Constraints from Stochastic Partially-Observed Closed-Loop Demonstrations",<br>   year = {2026}<br>}</pre></td>
</tr>

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
	<col width="18%" />
	<col width="2%" />
	<col width="80%" />
</colgroup>
<tbody>

<tr id="Skifstad26a">
	<td markdown="span"><br><img src="../images/icml_26_alqr_02.png" onmouseover="this.src='../images/icml_26_alqr_01.png'" onmouseout="this.src='../images/icml_26_alqr_02.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Local Linearity of LLMs Enables Activation Steering via Model-Based Linear Optimal Control** <br> 
		<em>Julian Skifstad, Xinyue Annie Yang, **Glen Chou**</em> <br> 
		 Proceedings of the 43rd International Conference on Machine Learning (ICML), July 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Skifstad26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Skifstad26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2604.19018)\] \[<a href="https://arxiv.org/pdf/2604.19018">PDF</a>\] \[<a href="https://github.com/trustworthyrobotics/lqr-activation-steering">Code</a>\] [<a href="javascript:toggleInfo(&#39;Skifstad26a&#39;,&#39;bibtex&#39;)">Cite</a>]<br>
    </td>
</tr>
<tr id="abs_Skifstad26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Inference-time LLM alignment methods, particularly activation steering, offer an alternative to fine-tuning by directly modifying activations during generation. Existing methods, however, often rely on non-anticipative interventions that ignore how perturbations propagate through transformer layers and lack online error feedback, resulting in suboptimal, open-loop control. To address this, we show empirically that, despite the nonlinear structure of transformer blocks, layer-wise dynamics across multiple LLM architectures and scales are well-approximated by locally-linear models. Exploiting this property, we model LLM inference as a linear time-varying dynamical system and adapt the classical linear quadratic regulator to compute feedback controllers using layer-wise Jacobians, steering activations toward desired semantic setpoints in closed-loop with minimal computational overhead and no offline training. We also derive theoretical bounds on setpoint tracking error, enabling formal guarantees on steering performance. Using a novel adaptive semantic feature setpoint signal, our method yields robust, fine-grained behavior control across models, scales, and tasks, including state-of-the-art modulation of toxicity, truthfulness, refusal, and arbitrary concepts, surpassing baseline steering methods. </div></td>
  </tr>
<tr id="bib_Skifstad26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Skifstad-ICML-26,<br>   Author = "Julian Skifstad, Xinyue Annie Yang, Glen Chou",
   journal = {Proceedings of the 43rd International Conference on Machine Learning (ICML)},<br>   Title = "Local Linearity of LLMs Enables Activation Steering via Model-Based Linear Optimal Control",<br>   year = {2026}<br>}</pre></td>
</tr>


<tr id="Fang26a">
	<td markdown="span"><br><img src="../images/rss_26_gpu.jpg" onmouseover="this.src='../images/rss_26_gpu.gif'" onmouseout="this.src='../images/rss_26_gpu.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Safe Large-Scale Robust Nonlinear MPC in Milliseconds via Reachability-Constrained System Level Synthesis on the GPU** <br> 
		<em>Jeffrey Fang, **Glen Chou**</em> <br> 
		 Proceedings of Robotics: Science and Systems (RSS) XXII, July 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Fang26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Fang26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2604.07644)\] \[<a href="https://arxiv.org/pdf/2604.07644">PDF</a>\] \[<a href="https://trustworthyrobotics.github.io/gpu_sls_site/">Project Website</a>\] \[<a href="https://github.com/Jeff300fang/gpu_sls">Code</a>\] \[<a href="https://www.youtube.com/watch?v=JbViVhenPTw">Video</a>\] [<a href="javascript:toggleInfo(&#39;Fang26a&#39;,&#39;bibtex&#39;)">Cite</a>]<br>
    </td>
</tr>
<tr id="abs_Fang26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present GPU-SLS, a GPU-parallelized framework for safe, robust nonlinear model predictive control (MPC) that scales to high-dimensional uncertain robotic systems and long planning horizons. Our method jointly optimizes an inequality-constrained, dynamically-feasible nominal trajectory, a tracking controller, and a closed-loop reachable set under disturbance, all in real-time. To efficiently compute nominal trajectories, we develop a sequential quadratic programming procedure with a novel GPU-accelerated quadratic program (QP) solver that uses parallel associative scans and adaptive caching within an alternating direction method of multipliers (ADMM) framework. The same GPU QP backend is used to optimize robust tracking controllers and closed-loop reachable sets via system level synthesis (SLS), enabling reachability-constrained control in both fixed- and receding-horizon settings. We achieve substantial performance gains, reducing nominal trajectory solve times by 97.7% relative to state-of-the-art CPU solvers and 71.8% compared to GPU solvers, while accelerating SLS-based control and reachability by 237x. Despite large problem scales, our method achieves 100% empirical safety, unlike high-dimensional learning-based reachability baselines. We validate our approach on complex nonlinear systems, including whole-body quadrupeds (61D) and humanoids (75D), synthesizing robust control policies online on the GPU in 20 milliseconds on average and scaling to problems with 2 x 10^5 decision variables and 8 x 10^4 constraints. </div></td>
  </tr>
<tr id="bib_Fang26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Fang-RSS-26,<br>   Author = "Jeffrey Fang, Glen Chou",
   journal = {Proceedings of Robotics: Science and Systems (RSS) XXII},<br>   Title = "Safe Large-Scale Robust Nonlinear MPC in Milliseconds via Reachability-Constrained System Level Synthesis on the GPU",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Li26b">
	<td markdown="span"><br><img src="../images/rss_26_contact.jpg" onmouseover="this.src='../images/rss_26_contact.gif'" onmouseout="this.src='../images/rss_26_contact.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Certified Gradient-Based Contact-Rich Manipulation via Smoothing-Error Reachable Tubes** <br> 
		<em>Wei-Chen Li, **Glen Chou**</em> <br> 
		 Proceedings of Robotics: Science and Systems (RSS) XXII, July 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Li26b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Li26b&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2602.09368)\] \[<a href="https://arxiv.org/pdf/2602.09368">PDF</a>\] \[<a href="https://trustworthyrobotics.github.io/quasistatic-contact-SLS/">Project Website</a>\] \[<a href="https://github.com/trustworthyrobotics/quasistatic-contact-SLS">Code</a>\] \[<a href="https://www.youtube.com/watch?v=LFxi2hkQJyo&pp=0gcJCT4LAYcqIYzv">Video</a>\] [<a href="javascript:toggleInfo(&#39;Li26b&#39;,&#39;bibtex&#39;)">Cite</a>]<br>
    </td>
</tr>
<tr id="abs_Li26b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Gradient-based methods can efficiently optimize controllers using physical priors and differentiable simulators, but contact-rich manipulation remains challenging due to discontinuous or vanishing gradients from hybrid contact dynamics. Smoothing the dynamics yields continuous gradients, but the resulting model mismatch can cause controller failures when executed on real systems. We address this trade-off by planning with smoothed dynamics while explicitly quantifying and compensating for the induced errors, providing formal guarantees of constraint satisfaction and goal reachability on the true hybrid dynamics. Our method smooths both contact dynamics and geometry via a novel differentiable simulator based on convex optimization, which enables us to characterize the discrepancy from the true dynamics as a set-valued deviation. This deviation constrains the optimization of time-varying affine feedback policies through analytical bounds on the system's reachable set, enabling robust constraint satisfaction guarantees for the true closed-loop hybrid dynamics, while relying solely on informative gradients from the smoothed dynamics. We evaluate our method on several contact-rich tasks, including planar pushing, object rotation, and in-hand dexterous manipulation, achieving guaranteed constraint satisfaction with lower safety violation and goal error than baselines. By bridging differentiable physics with set-valued robust control, our method is the first certifiable gradient-based policy synthesis method for contact-rich manipulation. </div></td>
  </tr>
<tr id="bib_Li26b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Li-RSS-26,<br>   Author = "Wei-Chen Li, Glen Chou",
   journal = {Proceedings of Robotics: Science and Systems (RSS) XXII},<br>   Title = "Certified Gradient-Based Contact-Rich Manipulation via Smoothing-Error Reachable Tubes",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Shen26a">
	<td markdown="span"><br><img src="../images/rss_26_taylor.jpg" onmouseover="this.src='../images/rss_26_taylor.gif'" onmouseout="this.src='../images/rss_26_taylor.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Parallel Differentiable Reachability for Learning and Planning with Certified Neural Dynamics and Controllers** <br> 
		<em>Keyi Shen, **Glen Chou**</em> <br> 
		 Proceedings of Robotics: Science and Systems (RSS) XXII, July 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Shen26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Shen26a&#39;); ">Abstract</a>]
                \[[arXiv](TBD)\] \[<a href="TBD">PDF</a>\] \[<a href="https://trustworthyrobotics.github.io/diffreach_site/">Project Website</a>\] \[<a href="https://github.com/trustworthyrobotics/DiffReach">Code (DiffReach)</a>\] \[<a href="https://github.com/trustworthyrobotics/DiffReach-Robotics">Code (DiffReach-Robotics)</a>\] \[<a href="https://www.youtube.com/watch?v=E6zeKt26TcM&pp=0gcJCT4LAYcqIYzv">Video</a>\] [<a href="javascript:toggleInfo(&#39;Shen26a&#39;,&#39;bibtex&#39;)">Cite</a>]<br>
    </td>
</tr>
<tr id="abs_Shen26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Neural network (NN) dynamics models and control policies achieve strong performance in robotics, but providing sound guarantees under uncertainty is difficult, especially when the NNs are components within the closed-loop system. Existing reachability tools offer formal over-approximations, yet are often non-differentiable, overly conservative, and too slow to integrate into modern learning and real-time planning pipelines. To address this, we present a parallelizable, differentiable reachability analysis tool in JAX that unifies continuous- and discrete-time systems and supports both analytical and NN-based dynamics and controllers. Our reachability tool uses Taylor-model flowpipe construction and CROWN-style linear bound relaxation and propagation, yielding a GPU-batched reachability primitive that can be differentiated and used in downstream objectives. Building on this primitive, we design (i) a certified training method that encourages the learning of reachability-friendly dynamics models and controllers, and (ii) a reachability-informed sampling-based MPC scheme that incorporates certified reachable sets during action selection and enables gradient-based refinement. Experiments on non-prehensile object manipulation and quadrotor control tasks show competitive performance to baseline planners while providing tight, certified reachability guarantees under uncertainty. </div></td>
  </tr>
<tr id="bib_Shen26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Shen-RSS-26,<br>   Author = "Keyi Shen, Glen Chou",
   journal = {Proceedings of Robotics: Science and Systems (RSS) XXII},<br>   Title = "Parallel Differentiable Reachability for Learning and Planning with Certified Neural Dynamics and Controllers",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Leeman26a">
	<td markdown="span"><br><img src="../images/rss_26_vision.jpg" onmouseover="this.src='../images/rss_26_vision.gif'" onmouseout="this.src='../images/rss_26_vision.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**VISION-SLS: Safe Perception-Based Control from Learned Visual Representations via System Level Synthesis** <br> 
		<em>Antoine Leeman\*, Shuyu Zhan\*, Melanie Zeilinger, **Glen Chou**</em> <br> 
		 Proceedings of Robotics: Science and Systems (RSS) XXII, July 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Leeman26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Leeman26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2604.24894)\] \[<a href="https://arxiv.org/pdf/2604.24894">PDF</a>\] \[<a href="https://trustworthyrobotics.github.io/VISION-SLS/">Project Website</a>\] \[<a href="https://github.com/trustworthyrobotics/VISION-SLS">Code</a>\] \[<a href="https://www.youtube.com/watch?v=a07cRhBb3xc&pp=0gcJCT4LAYcqIYzv">Video</a>\] [<a href="javascript:toggleInfo(&#39;Leeman26a&#39;,&#39;bibtex&#39;)">Cite</a>]<br>
    </td>
</tr>
<tr id="abs_Leeman26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We propose VISION-SLS, a method for nonlinear output-feedback control from high-resolution RGB images which provides robust constraint satisfaction guarantees under calibrated uncertainty bounds despite partial observability, sensor noise, and nonlinear dynamics. To enable scalability while retaining guarantees, we propose: (i) a learned low-dimensional observation map from pretrained visual features with state-dependent error bounds, and (ii) a causal affine time-varying output-feedback policy optimized via System Level Synthesis (SLS). We develop a scalable, novel solver for the resulting nonconvex program that leverages sequential convex programming coupled with efficient Riccati recursions. On two simulated visuomotor tasks (a 4D car and a 10D quadrotor) with >= 512 x 512 pixels and a 59D humanoid task with partial observability, our method enables safe, information-gathering behavior that reduces uncertainty while guaranteeing constraint satisfaction with empirically-calibrated error bounds. We also validate our method on hardware, safely controlling a ground vehicle from onboard images, outperforming baselines in safety rate and solve times. Together, these results show that learned visual abstractions coupled with an efficient solver make SLS-based safe visuomotor output-feedback practical at scale.</div></td>
  </tr>
<tr id="bib_Leeman26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Leeman-RSS-26,<br>   Author = "Antoine Leeman, Shuyu Zhan, Melanie Zeilinger, Glen Chou",
   journal = {Proceedings of Robotics: Science and Systems (RSS) XXII},<br>   Title = "VISION-SLS: Safe Perception-Based Control from Learned Visual Representations via System Level Synthesis",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Nath26b">
	<td markdown="span"><br><img src="../images/l4dc26_koop.jpg" onmouseover="this.src='../images/l4dc26_koop.gif'" onmouseout="this.src='../images/l4dc26_koop.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Scalable Data-Driven Reachability Analysis and Control via Koopman Operators with Conformal Coverage Guarantees** <br> 
		<em>Devesh Nath\*, Haoran Yin\*, **Glen Chou**</em> <br> 
		 Proceedings of the 8th Annual Learning for Dynamics & Control Conference (L4DC), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Nath26b&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Nath26b&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2601.01076)\] \[<a href="https://arxiv.org/pdf/2601.01076">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Nath26b&#39;,&#39;bibtex&#39;)">Cite</a>]<br>
        <b><span style="color:red">Selected for oral presentation, top 10.3% of accepted papers.</span></b>
    </td>
</tr>
<tr id="abs_Nath26b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We propose a scalable reachability-based framework for probabilistic, data-driven safety verification of unknown nonlinear dynamics. We use Koopman theory with a neural network (NN) lifting function to learn an approximate linear representation of the dynamics and design linear controllers in this space to enable closed-loop tracking of a reference trajectory distribution. Closed-loop reachable sets are efficiently computed in the lifted space and mapped back to the original state space via NN verification tools. To capture model mismatch between the Koopman dynamics and the true system, we apply conformal prediction to produce statistically-valid error bounds that inflate the reachable sets to ensure the true trajectories are contained with a user-specified probability. These bounds generalize across references, enabling reuse without recomputation. Results on high-dimensional MuJoCo tasks (11D Hopper, 28D Swimmer) and 12D quadcopters show improved reachable set coverage rate, computational efficiency, and conservativeness over existing methods. </div></td>
  </tr>
<tr id="bib_Nath26b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Nath-L4DC-26,<br>   Author = "Devesh Nath, Haoran Yin, Glen Chou",
   journal = {Proceedings of the 8th Annual Learning for Dynamics & Control Conference (L4DC)},<br>   Title = "Scalable Data-Driven Reachability Analysis and Control via Koopman Operators with Conformal Coverage Guarantees",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Srinivasan26a">
	<td markdown="span"><br><img src="../images/l4dc26_cp.jpg" onmouseover="this.src='../images/l4dc26_cp.gif'" onmouseout="this.src='../images/l4dc26_cp.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Safety Beyond the Training Data: Robust Out-of-Distribution MPC via Conformalized System Level Synthesis** <br> 
		<em>Anutam Srinivasan, Antoine Leeman, **Glen Chou**</em> <br> 
		 Proceedings of the 8th Annual Learning for Dynamics & Control Conference (L4DC), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Srinivasan26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Srinivasan26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2602.12047)\] \[<a href="https://arxiv.org/pdf/2602.12047">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Srinivasan26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Srinivasan26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a novel framework for robust out-of-distribution planning and control using conformal prediction (CP) and system level synthesis (SLS), addressing the challenge of ensuring safety and robustness when using learned dynamics models beyond the training data distribution. We first derive high-confidence model error bounds using weighted CP with a learned, state-control-dependent covariance model. These bounds are integrated into an SLS-based robust nonlinear model predictive control (MPC) formulation, which performs constraint tightening over the prediction horizon via volume-optimized forward reachable sets. We provide theoretical guarantees on coverage and robustness under distributional drift, and analyze the impact of data density and trajectory tube size on prediction coverage. Empirically, we demonstrate our method on nonlinear systems of increasing complexity, including a 4D car and a {12D} quadcopter, improving safety and robustness compared to fixed-bound and non-robust baselines, especially outside of the data distribution. </div></td>
  </tr>
<tr id="bib_Srinivasan26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Srinivasan-L4DC-26,<br>   Author = "Anutam Srinivasan, Antoine Leeman, Glen Chou",
   journal = {Proceedings of the 8th Annual Learning for Dynamics & Control Conference (L4DC)},<br>   Title = "Safety Beyond the Training Data: Robust Out-of-Distribution MPC via Conformalized System Level Synthesis",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Qiu26a">
	<td markdown="span"><br><img src="../images/l4dc_26_cl_01.png" onmouseover="this.src='../images/l4dc_26_cl_02.png'" onmouseout="this.src='../images/l4dc_26_cl_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Active Constraint Learning in High Dimensions from Demonstrations** <br> 
		<em>Zheng Qiu, Chih-Yuan Chiu, **Glen Chou**</em> <br> 
		 Proceedings of the 8th Annual Learning for Dynamics & Control Conference (L4DC), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Qiu26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Qiu26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2512.22757)\] \[<a href="https://arxiv.org/pdf/2512.22757">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Qiu26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Qiu26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present an iterative active constraint learning (ACL) algorithm, within the learning from demonstrations (LfD) paradigm, which intelligently solicits informative demonstration trajectories for inferring an unknown constraint in the demonstrator's environment. Our approach iteratively trains a Gaussian process (GP) on the available demonstration dataset to represent the unknown constraints, uses the resulting GP posterior to query start/goal states, and generates informative demonstrations which are added to the dataset. Across simulation and hardware experiments using high-dimensional nonlinear dynamics and unknown nonlinear constraints, our method outperforms a baseline, random-sampling based method at accurately performing constraint inference from an iteratively generated set of sparse but informative demonstrations. </div></td>
  </tr>
<tr id="bib_Qiu26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Qiu-L4DC-26,<br>   Author = "Zheng Qiu, Chih-Yuan Chiu, Glen Chou",
   journal = {Proceedings of the 8th Annual Learning for Dynamics & Control Conference (L4DC)},<br>   Title = "Active Constraint Learning in High Dimensions from Demonstrations",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Huang26a">
	<td markdown="span"><br><img src="../images/cvpr26_maps.jpg" onmouseover="this.src='../images/cvpr26_maps.gif'" onmouseout="this.src='../images/cvpr26_maps.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**MAPS: Preserving Vision-Language Representations via Module-Wise Proximity Scheduling for Better Vision-Language-Action Generalization** <br> 
		<em>Chengyue Huang\*, Mellon M. Zhang\*, Robert Azarcon, **Glen Chou**, Zsolt Kira</em> <br> 
		 Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Huang26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Huang26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2511.19878)\] \[<a href="https://arxiv.org/pdf/2511.19878">PDF</a>\] \[<a href="https://mapsvla.github.io/">Project Website</a>\] \[<a href="https://github.com/chengyuehuang511/MAPS-VLA">Code</a>\] [<a href="javascript:toggleInfo(&#39;Huang26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Huang26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Vision-Language-Action (VLA) models inherit strong priors from pretrained Vision-Language Models (VLMs), but naive fine-tuning often disrupts these representations and harms generalization. Existing fixes -- freezing modules or applying uniform regularization -- either overconstrain adaptation or ignore the differing roles of VLA components. We present MAPS (Module-Wise Proximity Scheduling), the first robust fine-tuning framework for VLAs. Through systematic analysis, we uncover an empirical order in which proximity constraints should be relaxed to balance stability and flexibility. MAPS linearly schedules this relaxation, enabling visual encoders to stay close to their pretrained priors while action-oriented language layers adapt more freely. MAPS introduces no additional parameters or data, and can be seamlessly integrated into existing VLAs. Across MiniVLA-VQ, MiniVLA-OFT, OpenVLA-OFT, and challenging benchmarks such as SimplerEnv, CALVIN, LIBERO, as well as real-world evaluations on the Franka Emika Panda platform, MAPS consistently boosts both in-distribution and out-of-distribution performance (up to +30%). Our findings highlight empirically guided proximity to pretrained VLMs as a simple yet powerful principle for preserving broad generalization in VLM-to-VLA transfer. </div></td>
  </tr>
<tr id="bib_Huang26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Huang-CVPR-26,<br>   Author = "Chengyue Huang, Mellon M. Zhang, Robert Azarcon, Glen Chou, Zsolt Kira",
   journal = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},<br>   Title = "MAPS: Preserving Vision-Language Representations via Module-Wise Proximity Scheduling for Better Vision-Language-Action Generalization",<br>   year = {2026}<br>}</pre></td>
</tr>


<tr id="Li26a">
	<td markdown="span"><br><img src="../images/icra26_convex.jpg" onmouseover="this.src='../images/icra26_convex.gif'" onmouseout="this.src='../images/icra26_convex.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**A Convex Formulation of Compliant Contact between Filaments and Rigid Bodies** <br> 
		<em>Wei-Chen Li, **Glen Chou**</em> <br> 
		 Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Li26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Li26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2509.13434)\] \[<a href="https://arxiv.org/pdf/2509.13434">PDF</a>\] \[<a href="https://github.com/wei-chen-li/drake-DER">Code</a>\] \[<a href="https://www.youtube.com/watch?v=EZtgBe6Hdfo">Video</a>\] [<a href="javascript:toggleInfo(&#39;Li26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Li26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a computational framework for simulating filaments interacting with rigid bodies through contact. Filaments are challenging to simulate due to their codimensionality, i.e., they are one-dimensional structures embedded in three-dimensional space. Existing methods often assume that filaments remain permanently attached to rigid bodies. Our framework unifies discrete elastic rod (DER) modeling, a pressure field patch contact model, and a convex contact formulation to accurately simulate frictional interactions between slender filaments and rigid bodies - capabilities not previously achievable. Owing to the convex formulation of contact, each time step can be solved to global optimality, guaranteeing complementarity between contact velocity and impulse. We validate the framework by assessing the accuracy of frictional forces and comparing its physical fidelity against baseline methods. Finally, we demonstrate its applicability in both soft robotics, such as a stochastic filament-based gripper, and deformable object manipulation, such as shoelace tying, providing a versatile simulator for systems involving complex filament-filament and filament-rigid body interactions. </div></td>
  </tr>
<tr id="bib_Li26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Li-ICRA-26,<br>   Author = "Wei-Chen Li, Glen Chou",
   journal = {Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "A Convex Formulation of Compliant Contact between Filaments and Rigid Bodies",<br>   year = {2026}<br>}</pre></td>
</tr>


<tr id="Muenprasitivej26a">
	<td markdown="span"><br><img src="../images/icra26_cp.jpg" onmouseover="this.src='../images/icra26_cp.gif'" onmouseout="this.src='../images/icra26_cp.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Probabilistically-Safe Bipedal Navigation over Uncertain Terrain via Conformal Prediction and Contraction Analysis** <br> 
		<em>Kasidit Muenprasitivej, Ye Zhao, **Glen Chou**</em> <br> 
		 Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Muenprasitivej26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Muenprasitivej26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2510.07725)\] \[<a href="https://arxiv.org/pdf/2510.07725">PDF</a>\] \[<a href="https://www.youtube.com/watch?v=ntlGhmgGbhw">Video</a>\] [<a href="javascript:toggleInfo(&#39;Muenprasitivej26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Muenprasitivej26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We address the challenge of enabling bipedal robots to traverse rough terrain by developing probabilistically safe planning and control strategies that ensure dynamic feasibility and centroidal robustness under terrain uncertainty. Specifically, we propose a high-level Model Predictive Control (MPC) navigation framework for a bipedal robot with a specified confidence level of safety that (i) enables safe traversal toward a desired goal location across a terrain map with uncertain elevations, and (ii) formally incorporates uncertainty bounds into the centroidal dynamics of locomotion control. To model the rough terrain, we employ Gaussian Process (GP) regression to estimate elevation maps and leverage Conformal Prediction (CP) to construct calibrated confidence intervals that capture the true terrain elevation. Building on this, we formulate contraction-based reachable tubes that explicitly account for terrain uncertainty, ensuring state convergence and tube invariance. In addition, we introduce a contraction-based flywheel torque control law for the reduced-order Linear Inverted Pendulum Model (LIPM), which stabilizes the angular momentum about the center-of-mass (CoM). This formulation provides both probabilistic safety and goal reachability guarantees. For a given confidence level, we establish the forward invariance of the proposed torque control law by demonstrating exponential stabilization of the actual CoM phase-space trajectory and the desired trajectory prescribed by the high-level planner. Finally, we evaluate the effectiveness of our planning framework through physics-based simulations of the Digit bipedal robot in MuJoCo. </div></td>
  </tr>
<tr id="bib_Muenprasitivej26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Muenprasitivej-ICRA-26,<br>   Author = "Kasidit Muenprasitivej, Ye Zhao, Glen Chou",
   journal = {Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "Probabilistically-Safe Bipedal Navigation over Uncertain Terrain via Conformal Prediction and Contraction Analysis",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Zhan26a">
	<td markdown="span"><br><img src="../images/icra26_multisls.jpg" onmouseover="this.src='../images/icra26_multisls.gif'" onmouseout="this.src='../images/icra26_multisls.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Robustly Constrained Dynamic Games for Uncertain Nonlinear Dynamics** <br> 
		<em>Shuyu Zhan\*, Chih-Yuan Chiu\*, Antoine Leeman, **Glen Chou**</em> <br> 
		 Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Zhan26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Zhan26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2509.16826)\] \[<a href="https://arxiv.org/pdf/2509.16826">PDF</a>\] \[<a href="https://github.com/trustworthyrobotics/Robust-Dynamic-Game-SLS">Code</a>\] \[<a href="https://www.youtube.com/watch?v=fzOfpO_ugsc">Video</a>\] [<a href="javascript:toggleInfo(&#39;Zhan26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Zhan26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We propose a novel framework for robust dynamic games with nonlinear dynamics corrupted by state-dependent additive noise, and nonlinear agent-specific and shared constraints. Leveraging system-level synthesis (SLS), each agent designs a nominal trajectory and a causal affine error feedback law to minimize their own cost while ensuring that its own constraints and the shared constraints are satisfied, even under worst-case noise realizations. Building on these nonlinear safety certificates, we define the novel notion of a robustly constrained Nash equilibrium (RCNE). We then present an Iterative Best Response (IBR)-based algorithm that iteratively refines the optimal trajectory and controller for each agent until approximate convergence to the RCNE. We evaluated our method on simulations and hardware experiments involving large numbers of robots with high-dimensional nonlinear dynamics, as well as state-dependent dynamics noise. Across all experiment settings, our method generated trajectory rollouts which robustly avoid collisions, while a baseline game-theoretic algorithm for producing open-loop motion plans failed to generate trajectories that satisfy constraints. </div></td>
  </tr>
<tr id="bib_Zhan26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Zhan-ICRA-26,<br>   Author = "Shuyu Zhan, Chih-Yuan Chiu, Antoine Leeman, Glen Chou",
   journal = {Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "Robustly Constrained Dynamic Games for Uncertain Nonlinear Dynamics",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Nath26a">
	<td markdown="span"><br><img src="../images/icra26_sagemp.jpg" onmouseover="this.src='../images/icra26_sagemp.gif'" onmouseout="this.src='../images/icra26_sagemp.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Formal Safety Verification and Refinement for Generative Motion Planners via Certified Local Stabilization** <br> 
		<em>Devesh Nath\*, Haoran Yin\*, **Glen Chou**</em> <br> 
		 Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;Nath26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Nath26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2509.19688)\] \[<a href="https://arxiv.org/pdf/2509.19688">PDF</a>\] \[<a href="https://www.youtube.com/watch?v=K8ppu6AaOxw">Video</a>\] [<a href="javascript:toggleInfo(&#39;Nath26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_Nath26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for formal safety verification of learning-based generative motion planners. Generative motion planners (GMPs) offer advantages over traditional planners, but verifying the safety and dynamic feasibility of their outputs is difficult since neural network verification (NNV) tools scale only to a few hundred neurons, while GMPs often contain millions. To preserve GMP expressiveness while enabling verification, our key insight is to imitate the GMP by stabilizing references sampled from the GMP with a small neural tracking controller and then applying NNV to the closed-loop dynamics. This yields reachable sets that rigorously certify closed-loop safety, while the controller enforces dynamic feasibility. Building on this, we construct a library of verified GMP references and deploy them online in a way that imitates the original GMP distribution whenever it is safe to do so, improving safety without retraining. We evaluate across diverse planners, including diffusion, flow matching, and vision-language models, improving safety in simulation (on ground robots and quadcopters) and on hardware (differential-drive robot). </div></td>
  </tr>
<tr id="bib_Nath26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Nath-ICRA-26,<br>   Author = "Devesh Nath, Haoran Yin, Glen Chou",
   journal = {Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "Formal Safety Verification and Refinement for Generative Motion Planners via Certified Local Stabilization",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="He26a">
	<td markdown="span"><br><img src="../images/icra26_navmoe.jpg" onmouseover="this.src='../images/icra26_navmoe.gif'" onmouseout="this.src='../images/icra26_navmoe.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**NavMoE: Hybrid Model-and Learning-based Traversability Estimation for Local Navigation via Mixture of Experts** <br> 
		<em>Botao He\*, Amir H. Shahidzadeh\*, Yu Chen\*, Jiayi Wu, Tianrui Guan, Guofei Chen, Howie Choset, Dinesh Manocha, **Glen Chou**, Cornelia Fermuller, Yiannis Aloimonos</em> <br> 
		 Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA), June 2026. <br>
		[<a href="javascript:toggleInfo(&#39;He26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/He26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2509.12747)\] \[<a href="https://arxiv.org/pdf/2509.12747">PDF</a>\] \[<a href="https://www.youtube.com/watch?v=D9CSTXQi0Wk&pp=0gcJCcMKAYcqIYzv">Video</a>\] [<a href="javascript:toggleInfo(&#39;He26a&#39;,&#39;bibtex&#39;)">Cite</a>]
    </td>
</tr>
<tr id="abs_He26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: This paper explores traversability estimation for robot navigation. A key bottleneck in traversability estimation lies in efficiently achieving reliable and robust predictions while accurately encoding both geometric and semantic information across diverse environments. We introduce Navigation via Mixture of Experts (NAVMOE), a hierarchical and modular approach for traversability estimation and local navigation. NAVMOE combines multiple specialized models for specific terrain types, each of which can be either a classical model-based or a learning-based approach that predicts traversability for specific terrain types. NAVMOE dynamically weights the contributions of different models based on the input environment through a gating network. Overall, our approach offers three advantages: First, NAVMOE enables traversability estimation to adaptively leverage specialized approaches for different terrains, which enhances generalization across diverse and unseen environments. Second, our approach significantly improves efficiency with negligible cost of solution quality by introducing a training-free lazy gating mechanism, which is designed to minimize the number of activated experts during inference. Third, our approach uses a two-stage training strategy that enables the training for the gating networks within the hybrid MoE method that contains nondifferentiable modules. Extensive experiments show that NAVMOE delivers a better efficiency and performance balance than any individual expert or full ensemble across different domains, improving cross-domain generalization and reducing average computational cost by 81.2% via lazy gating, with less than a 2% loss in path quality. </div></td>
  </tr>
<tr id="bib_He26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{He-ICRA-26,<br>   Author = "Botao He, Amir Hossein Shahidzadeh, Yu Chen, Jiayi Wu, Tianrui Guan, Guofei Chen, Howie Choset, Dinesh Manocha, Glen Chou, Cornelia Fermuller, Yiannis Aloimonos",
   journal = {Proceedings of the 43rd IEEE International Conference on Robotics and Automation (ICRA)},<br>   Title = "NavMoE: Hybrid Model-and Learning-based Traversability Estimation for Local Navigation via Mixture of Experts",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="ZhangM26a">
	<td markdown="span"><br><img src="../images/wacv_26_01.png" onmouseover="this.src='../images/wacv_26_02.png'" onmouseout="this.src='../images/wacv_26_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Towards Streaming LiDAR Object Detection with Point Clouds as Egocentric Sequences** <br> 
		<em>Mellon M. Zhang, **Glen Chou\***, Saibal Mukhopadhyay\*</em> <br> 
		 Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV), March 2026. <br>
		[<a href="javascript:toggleInfo(&#39;ZhangM26a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/ZhangM26a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2506.06944)\] \[<a href="https://arxiv.org/pdf/2506.06944">PDF</a>\] \[<a href="https://github.com/meilongzhang/Polar-Hierarchical-Mamba">Code</a>\] [<a href="javascript:toggleInfo(&#39;ZhangM26a&#39;,&#39;bibtex&#39;)">Cite</a>] 
    </td>
</tr>
<tr id="abs_ZhangM26a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Accurate and low-latency 3D object detection is essential for autonomous driving, where safety hinges on both rapid response and reliable perception. While rotating LiDAR sensors are widely adopted for their robustness and fidelity, current detectors face a trade-off: streaming methods process partial polar sectors on the fly for fast updates but suffer from limited visibility, cross-sector dependencies, and distortions from retrofitted Cartesian designs, whereas fullscan methods achieve higher accuracy but are bottlenecked by the inherent latency of a LiDAR revolution. We propose Polar-Fast-Cartesian-Full (PFCF), a hybrid detector that combines fast polar processing for intra-sector feature extraction with accurate Cartesian reasoning for full-scene understanding. Central to PFCF is a custom Mamba SSMbased streaming backbone with dimensionally-decomposed convolutions that avoids distortion-heavy planes, enabling parameter-efficient, translation-invariant, and distortionrobust polar representation learning. Local sector features are extracted via this backbone, then accumulated into a sector feature buffer to enable efficient inter-sector communication through a full-scan backbone. PFCF establishes a new Pareto frontier on the Waymo Open dataset, surpassing prior streaming baselines by 10% mAP and matching full-scan accuracy at twice the update rate. Code is available at https://github.com/meilongzhang/PolarHierarchical-Mamba. </div></td>
  </tr>
<tr id="bib_ZhangM26a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Zhang-WACV-26,<br>   Author = "Mellon M. Zhang, Glen Chou, Saibal Mukhopadhyay",
   journal = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},<br>   Title = "Towards Streaming LiDAR Object Detection with Point Clouds as Egocentric Sequences",<br>   year = {2026}<br>}</pre></td>
</tr>



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

## Theses

<hr>

<table class="table">
<colgroup>
	<col width="18%" />
	<col width="2%" />
	<col width="80%" />
</colgroup>
<tbody>

<tr id="Chou22d">
	<td markdown="span"><br><img src="../images/auro_22_01.jpg" onmouseover="this.src='../images/wafr_22_01.jpg'" onmouseout="this.src='../images/auro_22_01.jpg'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Safe End-to-end Learning-based Robot Autonomy via Integrated Perception, Planning, and Control** <br> 
		<em>**Glen Chou**</em> <br> 
		PhD thesis, University of Michigan, August 2022. <br>
                [<a href="javascript:toggleInfo(&#39;Chou22d&#39;,&#39;abstract&#39;)">Abstract</a>] \[[PDF](https://glenchou.github.io/papers/chou_thesis.pdf)\] [<a href="javascript:toggleInfo(&#39;Chou22d&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou22d" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Trustworthy robots must be able to complete tasks reliably while obeying safety constraints. While traditional methods for constrained motion planning and optimal control can achieve this if the environment is accurately modeled and the task is unambiguous, future robots will be deployed in unstructured settings with poorly-understood or inaccurate dynamics, observation models, and task specifications. Thus, to plan and perform control, robots will invariably need data to learn and refine their understanding of their environments and tasks. Though machine learning provides a means to obtain perception and dynamics models from data, blindly trusting these potentially-unreliable models when planning can cause unsafe and unpredictable behavior at runtime. To this end, this dissertation is motivated by the following questions: (1) To refine their understanding of the desired task, how can robots learn components of a constrained motion planner (e.g., constraints, task specifications) in a data-efficient manner? and (2) How can robots quantify and remain robust to the inevitable uncertainty and error in learned components within the broader perception-planning-control autonomy loop in order to provide system-level guarantees on safety and task completion at runtime?

To address the first question, we propose methods that use successful human demonstrations to learn unknown constraints and task specifications. The crux of this problem relies on learning what not to do (i.e., behavior violating the unknown constraints or specifications) from only successful examples. We make the insight that the demonstrations' approximate optimality implicitly defines what the robot should not do, and that this information can be extracted by simulating lower-cost trajectories and by using the Karush-Kuhn-Tucker (KKT) optimality conditions. These strong optimality priors make our method highly data-efficient. We use these methods to learn a broad class of constraints, including nonconvex obstacle constraints, and linear temporal logic formulas, which can describe complex temporally-extended robotic tasks. We demonstrate that our constraint-learning methods scale to high-dimensional systems, e.g., learning to complete novel constrained navigation tasks for a simulated 12D quadrotor and multi-stage manipulation tasks on a 7DOF arm (both simulated and in the real world).

To address the second question, we develop methods addressing uncertainty in A) constraints learned from demonstrations and B) dynamics models and perception modules learned from data. To quantify constraint uncertainty, we extract the set of constraints that are consistent with the demonstrations' KKT conditions (i.e., a belief over constraints), which is done by solving a sequence of robust mixed integer programs. We show that the robot can plan probabilistically-safe trajectories using this constraint belief, which can be updated using constraint data gathered in execution. To address uncertainty when planning with learned dynamics models of underactuated systems controlled with high-dimensional (image) observations, we estimate bounds on the error of the learned models inside a domain around their training data. Using tools from contraction theory, we propagate this model error bound into a trajectory tracking error bound. This tracking bound is used to constrain the planner to only return plans that can be safely tracked, with high probability, in spite of the errors in the perception and dynamics. We demonstrate that these theoretical guarantees translate to success in simulation, enabling safe task completion at runtime on a variety of challenging high-dimensional, underactuated systems using rich sensor observations (e.g., RGB-D images) in the feedback control loop. </div></td>
  </tr>
<tr id="bib_Chou22d" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-Thesis-25,<br>   Author = "Glen Chou",
   journal = {PhD thesis, University of Michigan},<br>   Title = "Safe End-to-end Learning-based Robot Autonomy via Integrated Perception, Planning, and Control",<br>   year = {2022}<br>}</pre></td>
</tr>


</tbody>
</table>

<br>


## Refereed Workshop Papers/Technical Reports

<hr>

<table class="table">
<colgroup>
	<col width="18%" />
	<col width="2%" />
	<col width="80%" />
</colgroup>
<tbody>

<tr id="Zhang26b">
	<td markdown="span"><br><img src="../images/zhang26b.png" onmouseover="this.src='../images/zhang26b.png'" onmouseout="this.src='../images/zhang26b.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**On the Adversarial Robustness of Temporal LiDAR Object Detectors** <br> 
		<em>Mellon M. Zhang\*, Siddhant Panse\*, Akshal Dhal, Rishit Sarkar, Zimo Fan, **Glen Chou**</em> <br> 
		CVPR SPAR-3D Workshop: Security, Privacy, and Adversarial Robustness in 3D Generative Vision Models, June 2026. <br>
                [<a href="javascript:toggleInfo(&#39;Zhang26b&#39;,&#39;abstract&#39;)">Abstract</a>] \[[PDF](https://glenchou.github.io/papers/Zhang26b.pdf)\] [<a href="javascript:toggleInfo(&#39;Zhang26b&#39;,&#39;bibtex&#39;)">Cite</a>] <br> <b><span style="color:red">Best paper award, third place.</span></b> </td>
</tr>
<tr id="abs_Zhang26b" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Accurate 3D object detection is critical for autonomous driving, yet robustness to adversarial attacks -- such as LiDAR spoofing -- remains underexplored. While recent LiDAR-based detectors leverage temporal context to improve performance, they are only evaluated under benign conditions. In this work, we introduce ATLAS (Adversarial Temporal LiDAR Attack Suite), a large-scale, physically grounded benchmark for evaluating spoofing attacks on temporal detectors. ATLAS simulates realistic sensor-level attacks by injecting structured adversarial point clouds into multi-frame sequences. Our results reveal a counterintuitive trend: temporal models are consistently more vulnerable than single-frame baselines, with attack success rates increasing with memory length. We further observe systematic overconfidence on spoofed objects, indicating a failure to distinguish corrupted history from reliable inputs. Together, these findings show that temporal aggregation -- when built on the assumption of clean observations -- becomes a liability under adversarial perturbations, motivating the need for uncertainty-aware temporal perception. </div></td>
  </tr>
<tr id="bib_Zhang26b" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Zhang-CVPR-SPAR3D-26,<br>   Author = "Mellon M. Zhang, Siddhant Panse, Akshal Dhal, Rishit Sarkar, Zimo Fan, Glen Chou",
   journal = {CVPR SPAR-3D Workshop: Security, Privacy, and Adversarial Robustness in 3D Generative Vision Models},<br>   Title = "On the Adversarial Robustness of Temporal LiDAR Object Detectors",<br>   year = {2026}<br>}</pre></td>
</tr>

<tr id="Leeman25">
	<td markdown="span"><br><img src="../images/eurips_25_01.png" onmouseover="this.src='../images/eurips_25_01.png'" onmouseout="this.src='../images/eurips_25_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Epistemically Aware Predictive Visuomotor Control** <br> 
		<em>Antoine P. Leeman, Shuyu Zhan, Melanie Zeilinger\*, **Glen Chou\***</em> <br> 
		EurIPS Workshop on Epistemic Intelligence in Machine Learning, December 2025. <br>
                [<a href="javascript:toggleInfo(&#39;Leeman25&#39;,&#39;abstract&#39;)">Abstract</a>] \[[PDF](https://glenchou.github.io/papers/Leeman25.pdf)\] [<a href="javascript:toggleInfo(&#39;Leeman25&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Leeman25" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We design a safe visuomotor controller when perception is epistemically ambiguous due to occlusions, textureless regions, or distribution shift. Our approach is to replace point state estimates from images with credal (uncertainty) sets that a controller can leverage in real-time. To this end, we learn credal sets: a reduced measurement together with a state-dependent confidence set. We then design an ambiguity-aware output-feedback controller based on system level synthesis that treats it as a source of measurement ambiguity, propagates it through closed-loop responses, and enforces safety via uncertainty propagation and constraint tightening. The resulting pipeline links perception to control through sets, yielding certificates conditioned on coverage and naturally encouraging reducing epistemic uncertainty behavior. An efficient sequential convex programming implementation with Riccati recursions enables real-time control. In high-fidelity vision-based simulations of a car and a quadcopter, our method achieves safe trajectories in seconds while avoiding overconfidence under epistemic shift. </div></td>
  </tr>
<tr id="bib_Leeman25" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Leeman-EurIPS-25,<br>   Author = "Antoine P. Leeman, Shuyu Zhan, Melanie Zeilinger, Glen Chou",
   journal = {EurIPS Workshop on Epistemic Intelligence in Machine Learning},<br>   Title = "Epistemically Aware Predictive Visuomotor Control",<br>   year = {2025}<br>}</pre></td>
</tr>

<tr id="Zhang25">
	<td markdown="span"><br><img src="../images/wacv_26_01.png" onmouseover="this.src='../images/wacv_26_02.png'" onmouseout="this.src='../images/wacv_26_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Polar Hierarchical Mamba: Towards Streaming LiDAR Object Detection with Point Clouds as Egocentric Sequences** <br> 
		<em>Mellon M. Zhang, **Glen Chou**</em> <br> 
		IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) 4D Vision Workshop, June 2025. <br>
                [<a href="javascript:toggleInfo(&#39;Zhang25&#39;,&#39;abstract&#39;)">Abstract</a>] \[[PDF](https://glenchou.github.io/papers/Zhang25.pdf)\] [<a href="javascript:toggleInfo(&#39;Zhang25&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Zhang25" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: Accurate and efficient object detection is a crucial component for fully autonomous self-driving. LiDAR sensors are employed to augment or replace cameras for more robustness in diverse driving situations, making object detection on LiDAR point clouds a critical area of research and improvement. Traditional approaches to LiDAR object detection wait for a full 360 degree turn of the scanning sensor before processing the entire point cloud in one go, introducing significant latency and lowering throughput. Previous streaming approaches use the raw LiDAR polar coordinate system to process egocentric partial scans of point clouds, but rely on translation-invariant convolutions, which are incompatible with polar coordinates and lead to performance degradation. In this paper, we show that the reliance on convolutions is not necessary and propose a Mamba-only backbone with Polar Hierarchical Mamba (PHiM) blocks, aggregating per-point features within each partial scan with a local bidirectional state space model and capturing higher-level global features in a streaming fashion with a global forward state space model. Our model on the Waymo Open dataset demonstrates 10% performance improvement from the previous leading polar-based detector, featuring state of the art performance among all polar-based methods while being competitive with existing Cartesian-based detectors with a 2x improvement in processing throughput evaluated as predictions per second. </div></td>
  </tr>
<tr id="bib_Zhang25" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Zhang-CVPR4DV-25,<br>   Author = "Mellon M. Zhang, Glen Chou",
   journal = {IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) Workshop on 4D Vision},<br>   Title = "Polar Hierarchical Mamba: Towards Streaming LiDAR Object Detection with Point Clouds as Egocentric Sequences",<br>   year = {2025}<br>}</pre></td>
</tr>

<tr id="Chou22c">
	<td markdown="span"><br><img src="../images/rsspw_01.png" onmouseover="this.src='../images/rsspw_01.png'" onmouseout="this.src='../images/rsspw_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Safely Integrating Perception, Planning, and Control for Robust Learning-Based Robot Autonomy** <br> 
		<em>**Glen Chou**</em> <br> 
		Robotics: Science and Systems, Pioneers Workshop, June 2022. <br>
                [<a href="javascript:toggleInfo(&#39;Chou22c&#39;,&#39;abstract&#39;)">Abstract</a>] \[[PDF](https://glenchou.github.io/papers/Chou22c.pdf)\] [<a href="javascript:toggleInfo(&#39;Chou22c&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou22c" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>:  </div></td>
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
