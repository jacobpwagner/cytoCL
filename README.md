# cytoCL
Command line tools for cytolib
## Potential tools:
* FCS QC
  * cytofcscheck
  * cytofcs2h5
  * cytofcsswap
* flowJotoolset 
  * equivalent to flowJoWorkspace accessors, parser, gs accessors in R
  * cytoxmlls,cytoxml2gs, cytogsls, cytogsstats

## FCS QC discussion
* goal
	* perpare the fcs for the openCyto gating
		* consistent channels or markers
		* report low count outliers?
		* consistent critical keyword (used for pdata)
* check items
  * channel consistency
    * num of params
    * name			
	    * typo (fussy matching ?)
	    * case
  * marker
  * keyword
  	* supply a list of keys
  
*	QC report
	  * format
    * recommending standardizing solutions
    	* params
	      * swap chnls and markers
	      * drop redundant
	      * correct typos
      	* keywords
		* correct typos
		* report empty values?
      
* correct: (do we want to provide cli tools to do that?)
  * fcs is non-structural stream (data and txt is cat together) and designed for readonly
  * thus need to parse entire data and rewrite to new fcs/or h5? 
  * if so, maybe parse into h5 in the first place?
  * or direct user to do it in R by the tips from qc report
                          
