---
layout: page
title: Reliable Planning and Control with Learned Models
permalink: /projects/trusted_domain
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



Using learned dynamics models in the autonomy pipeline can reduce requirements on <em>a priori</em> knowledge. However, these models often fail to generalize when deployed in domains which they have not seen in training; thus, blindly trusting these models in planning may lead to unsafe and unpredictable runtime behavior. This project seeks to quantify where and to what extent these learned models can be trusted, in order to plan trajectories which ensure that the robot will behave safely and reliably at runtime. Achieving this requires an integrated, end-to-end safety analysis of the system, which entails propagating model error through planning and low-level feedback control. We show that leveraging model error representations based on Lipschitz constants and diffusion models within the planning and control loop enables safe, reliable planning with learned models, and that the theory translates to real-world reliability on hardware (e.g., manipulation, quadrotor flight, and ground vehicle navigation).

### <span style="font-weight:bold"> Selected publications:</span><br>

<table class="table">
<colgroup>
	<col width="30%" />
	<col width="2%" />
	<col width="68%" />
</colgroup>
<tbody>

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


