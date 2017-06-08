# MicroscopyClassifier
## Visualization and Classification of GFP-Labeled Proteins from Confocal and Widefield Microscopy Images Using Nearest Neighbor

### Introduction
Gene products may be tagged to study their localization, function, or structure. One method of gene product tagging is through CD-tagging. CD-tagging relies on the “Central Dogma” of molecular biology:

..1. DNA is copied through replication.

..2. mRNA is transcribed from DNA.

..3. Proteins are translated from mRNA.

A CD cassette is used to tag a gene of interest. This cassette contains the coding sequence for GFP (Green Fluorescent Protein), along with a splice acceptor and donor site. If correctly inserted into the intron of a gene, the coding sequence for GFP will be introduced into the mRNA transcript as a guest exon. When the mRNA is translated into its corresponding protein, GFP will be incorporated into the final protein structure.
	
GFP exhibits fluorescent properties, lending itself most useful for CD-tagging experiments. It absorbs light in the blue visible light spectra (450nm to 495nm) and emits light in the green visible light spectra (495nm to 570nm). GFP-tagged cells can be separated from non-tagged cells using flow cytometry. This technique sorts cells while suspended in a constant stream of liquid. The instrument possesses fluorescent detectors (among other detectors) that are able to differentiate between cells with and without fluorescent properties. In the case of CD-tagging, the excitation wavelength of the laser would be between 450nm and 495nm. The fluorescent detectors would look for events (cells) that emit light between 495nm and 570nm. These cells would be positive for GFP and separated from the non-GFP cells.
	
Various laser scanning microscopy techniques can be used to visualize the GFP-tagged proteins. Automated microscopes, such as Beckman Coulter IC100, allow multiple samples to be imaged at once. It collects widefield images of fluorescent cells. Confocal microscopes provide a higher level of contrast and produce an image with much less background noise. These images can be used to build classifiers that differentiate between various protein types and microcsopy techniques. 


### Materials and Methods
A few protein types of NIH-3T3 cells were tagged with GFP using CD-tagging. My cells were tagged with in an unknown protein B. The cells were cultured using a sterile technique. The hood, instruments, and media were sprayed with 70% ethanol before beginning tissue culture. The media was aspirated from the seed flask and 1 mL of trypsin was added. I aspirated the trypsin from the seed flask, then added another 1 mL of trypsin to the flask . After waiting for 3 to 5 minutes, I viewed the cells under the microscope to check that the trypsin had lifted the cells off the bottom of the flask.  Next, I added 5 mL of media to seed flask and to the new flask. There was a high density of cells in the seed flask so I only added 0.5 mL of cells from the seed flask to the new flask. The new flask was labeled then placed in the incubator. After 3 days, I repeated the cell culturing process. Since fewer cells were seen after sitting in trypsin, I increased the transfer volume from the seed flask to the new flask to 1 mL.

We used flow cytometry to separate the GFP tagged cells from the normal cells. The cells were prepared by first aspirating the media then allowing the cells to sit in trypsin for 5 minutes. Once the cells had lifted from the flask, 5 mL of media was added to the seed flask. The contents of the seed flask were then added to a 15 mL tube and centrifuged for 8 minutes. The media from the tube was aspirated then 1 mL of PBS was added and the contents were mixed.  The contents from the tube were added to a flow cytometry tube and then the cells were sorted. GFP tagged cells were sorted into one row of a 96 well plate (10 cells per well) and into a small dish (10 cells here, as well).

One week we imaged our cells using confocal and widefield (IC100) microscopes. The media was aspirated from the wells of the well plate and the small dish. We added 100 µL of dye to each well and the dish, then placed them under a dark bucket for at least 15 minutes to prevent photobleaching.  The well plate was loaded into the IC100, then the instrument was set up according to the specifications listed in appendix 1. The integration time was set to 2,000 msec with a gain of 70.  Images of the cells in the small dish were then taken using a confocal microscope. Finally, using these images as data, I developed a nearest neighbor classifier function in MATLAB to differentiate between confocal and widefield images as well as protein types. 
