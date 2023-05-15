# Holographic_localization
Algorithm fo indoor localization of passive RFID tags by Holographic method

The algorithm presented in the flowchart aims to describe the holographic localization of RFID passive tags in an indoor environment using four RFID readers.
The algorithm can be summarized as follows:

1- Initialization: 
The algorithm starts by initializing certain parameters such as readers step (Rs), grid section (Gs), the dimensions of the area (Adim), and the frequency (F) 
of the RFID system.

2- Tag Position Initialization:
The algorithm randomly selects a position for the tag within the defined area using the dimensions provided. It also initializes a hologram matrix (Hg) 
and sets the positions of the four readers (Pos_1, Pos_2, Pos_3, and Pos_4) at the corners of the area.

3- Iterative Process: The algorithm enters a loop where it performs the following steps iteratively:

        * Read Phase: The four readers perform a read operation to collect data from the RFID tags. The holograms obtained from each reader are denoted as H1, H2,
        H3,and H4.
        * Hologram Accumulation: The holograms obtained from each reader are added together to form a combined hologram matrix (H). This matrix is then 
        added to the general hologram matrix Hg which accumulates the hologram data over the iterations.
        * Position Update: The positions of the four readers are updated by moving them along the four sides of the localization area by a step (Rs): Reader 1 
        and Reader 3 are moving conversely and the same for reader 3 and 4.
        * Iteration Update: The iteration count (N) is decremented by 1.

4- Tag Localization: After the loop ends, the algorithm identifies the maximum pixel in the accumulated hologram matrix (Hg) to determine the estimated position
of the tag.
  
5- Localization Error Calculation: The algorithm calculates the localization error (LE) by measuring the Euclidean distance between the estimated tag position and
the real tag position.

This algorithm provides a systematic approach to localize RFID passive tags in an indoor environment using multiple readers. By iteratively collecting 
hologram data and updating reader positions, the algorithm aims to improve the accuracy of tag localization. The final estimated tag position is obtained by
analyzing the accumulated hologram data. The algorithm allows for the evaluation of the localization error and can be customized by adjusting the parameters 
based on specific requirements and constraints.
