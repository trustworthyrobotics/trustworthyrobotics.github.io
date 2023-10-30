---
layout: page
title: Fundamental Model-Based Tools for Verifiable Control
permalink: /projects/output_feedback
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


While data can help make our model-based tools for planning and control more calibrated to reality, we still lack sufficiently-strong model-based tools for verifiable behavior synthesis for many tasks in robotics, especially those involving contact-rich phenomena and imperfect perception from high-dimensional partial observations. This is a fundamental bottleneck to applying model-based tools in real-world applications like robotic manipulation. As such, in this line of work, I focus on strengthening our model-based control tools. I have studied 1) safe perception-based control from images, enabling end-to-end safe control from sensors, 2) scalable hybrid control techniques in the multi-agent setting, and 3) automatic corner-case generation for stress-testing complex controllers, e.g., from a real-world autonomous vehicle software stack.

### <span style="font-weight:bold"> Selected publications:</span><br>

<table class="table">
<colgroup>
	<col width="30%" />
	<col width="2%" />
	<col width="68%" />
</colgroup>
<tbody>


<tr id="Chou23a">
	<td markdown="span"><br><img src="../images/cdc_23_01.png" onmouseover="this.src='../images/cdc_23_02.gif'" onmouseout="this.src='../images/cdc_23_01.png'" />   </td>
	<td markdown="span"></td>
	<td markdown="span"><br>**Synthesizing Stable Reduced-Order Visuomotor Policies for Nonlinear Systems via Sums-of-Squares Optimization** <br> 
		<em>**Glen Chou**, Russ Tedrake</em> <br> 
		Proceedings of the 62nd IEEE Conference on Decision and Control (CDC), December 2023. <br>
		[<a href="javascript:toggleInfo(&#39;Chou23a&#39;,&#39;abstract&#39;)" onclick="javascript:pageTracker._trackPageview(&#39;/abstracts/Chou23a&#39;); ">Abstract</a>]
                \[[arXiv](https://arxiv.org/abs/2304.12405)\] \[<a href="https://arxiv.org/pdf/2304.12405.pdf">PDF</a>\] [<a href="javascript:toggleInfo(&#39;Chou23a&#39;,&#39;bibtex&#39;)">Cite</a>]</td>
</tr>
<tr id="abs_Chou23a" class="abstract noshow">
    <td colspan="3"><div align="justify"> <b>Abstract</b>: We present a method for synthesizing dynamic, reduced-order output-feedback polynomial control policies for control-affine nonlinear systems which guarantees runtime stability to a goal state, when using visual observations and a learned perception module in the feedback control loop. We leverage Lyapunov analysis to formulate the problem of synthesizing such policies. This problem is nonconvex in the policy parameters and the Lyapunov function that is used to prove the stability of the policy. To solve this problem approximately, we propose two approaches: the first solves a sequence of sum-of-squares optimization problems to iteratively improve a policy which is provably-stable by construction, while the second directly performs gradient-based optimization on the parameters of the polynomial policy, and its closed-loop stability is verified a posteriori. We extend our approach to provide stability guarantees in the presence of observation noise, which realistically arises due to errors in the learned perception module. We evaluate our approach on several underactuated nonlinear systems, including pendula and quadrotors, showing that our guarantees translate to empirical stability when controlling these systems from images, while baseline approaches can fail to reliably stabilize the system. </div></td>
  </tr>
<tr id="bib_Chou23a" class="bibtex noshow">
<td colspan="3"><b>BibTeX</b>:
  <pre>@inproceedings{Chou-CDC-23,<br>   Author = "Glen Chou and Russ Tedrake",
   journal = {Proceedings of the 62nd IEEE Conference on Decision and Control (CDC)},<br>   Title = "Synthesizing Stable Reduced-Order Visuomotor Policies for Nonlinear Systems via Sums-of-Squares Optimization",<br>   year = {2023}<br>}</pre></td>
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
