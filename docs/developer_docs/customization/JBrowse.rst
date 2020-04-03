
JBrowse
==========

We have changed the colours of our JBrowse to make it match KnowPulse for more seamless integration.
The following shows our customizations:

.. code-block:: css

	/* Change the color of the upper trapezoid */
	#GenomeBrowser.jbrowse div.locationTrap {
	  border-bottom-color: #17313E
	}
	#GenomeBrowser.jbrowse div.locationThumb {
	  border: 2px solid #17313E;
	}

	/* Change the color/Background of the top menu bar */
	#GenomeBrowser.jbrowse .menuBar {
	    background: url('http://knowpulse.usask.ca/portal/sites/all/themes/kptheme/images/mainbarbg.jpg') repeat-x;
	    text-align: right;
	}

	/** Customize HTML Features */
	#GenomeBrowser.jbrowse .feature2,
	  #GenomeBrowser.jbrowse .plus-feature2,
	  #GenomeBrowser.jbrowse .minus-feature2 {
	    height: 7px;
	    background-color: #62d335;
	}
	#GenomeBrowser.jbrowse .match_part,
	  #GenomeBrowser.jbrowse .plus-match_part,
	  #GenomeBrowser.jbrowse .minus-match_part {
	    height: 10px;
	    background-color: #00FF00;
	}
