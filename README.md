# 3D-KNIME-Pipeline
A series of KNIME workflows that perform virtual reactions of a defined 'scaffold' with commercial building blocks. Filtering of library with property filters, and selection of the most 3D compounds via PMI and USR analyis.

Overview

HTS and traditional virtual screening often suffer from low hit rates, one reason is due to the over-representation of flat molecules. This series of workflows aims to address these issues:

1. Piperidine reactions.knwf - takes a given scaffold and 'decorates' it using commercial buidling blocks. The products of each reaction are filtered according to a blend of the Ro5 and Veber's rules, along with an addition metric selecting compounds with a high fraction of sp3 atoms. Products that generate a new chiral centre are removed to limit diastereomer formation.
2. Principle moment of intertia commercial scaffold.knwf - Using the products generated from workflow 1, conformations of each compound are produced. The conformations are filtered to remove any that are not energetically accessible at standard temperatures. The conformations are then subjected to PMI analysis, and the percentage of conformations classifed as '3-dimensional' is calculated to isolate highly 3-D compounds.
3. Molecular shape comparison.knwf - using the highly 3-D compounds generated in workflow 2, the dataset is analysed using Ultrafast Shape Recognition (USR) to ensure that the 3-D dataset adopts a wide variety of shapes.


Tech Requirements

*Platform* KNIME Analytics Platform [https://www.knime.com/]
*Extensions* RDKit KNIME Integration, Vernalis KNIME Nodes, Community Cheminformatics Nodes


How to Use
1. Download this Repository
2. Import the files onto KNIME Analytics Platform
3. Execute the workflows sequentially
