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

<style>
    table.areas {
        display: table;
        text-align: center;
        margin: 0 auto;
    }
    table.areas tr {
        display: table-cell;
        width: 33%;
        border-radius: 5px;
        box-shadow: 0 0 25px 5px rgba(0,0,0,0.12);
    }
    table.areas tr:hover {
        background-color: rgba(0,117,97,0.2);
        cursor: pointer;
    }
    table.areas tr td {
        display: block;
    }
    table.areas tr td.ar_img {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 17em;
    }
    table.areas tr td.ar_img img {
        height:100%;
        object-fit: cover;
        padding-bottom: 0;
    }
    table.areas tr td.ar_text {
        display: block;
        height: 5em;
        vertical-align: top;
        padding-top: 0;
        padding-bottom: 1vh;
        line-height: 1;
    }
    @media screen and (max-width: 1024px) {
        table.areas tr {
            display: block;
            width: 100%; /* Set the width to 100% for smaller screens */
            box-sizing: border-box;
            margin-bottom: 10px; /* Adjust as needed */
        }
    }
</style>

<table class="areas">
        <tr onclick="window.location='constraints'">
                <td class="ar_img"><img src="/images/auro_22_02.gif" /></td>
                <td class="ar_text"><h2 style="font-size:1.5em"><a>Safely Learning Task Specifications <br> from Humans</a></h2></td>
        </tr>
        <tr onclick="window.location='trusted_domain'">
                <td class="ar_img"><img src="/images/icra_23b_alt.gif" /></td>
                <td class="ar_text"><h2 style="font-size:1.5em"><a>Reliable Planning and Control <br> with Learned Models</a></h2></td>
        </tr>
        <tr onclick="window.location='output_feedback'">
                <td class="ar_img"><img src="/images/isls.gif"/></td>
                <td class="ar_text"><h2 style="font-size:1.5em"><a>Fundamental Model-Based Tools <br> for Verifiable Control</a></h2></td>
        </tr>
</table>
