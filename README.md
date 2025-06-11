

Precision in the Dip: Improving True Thickness Calculation in Structurally Complex Coal Deposits
==============


N.J. Heckscher & B.J. Saunders

QEGSS Pty Ltd, Moranbah, Australia

ABSTRACT: Stratigraphic modelling within the Bowen Basin is frequently simplified by focusing on large-scale, economically dominant deposits where traditional methods, such as Independent Surfaces and Stacking, prove adequate. However, these methods often fail to accurately represent true stratigraphic thickness in the more structurally complex and economically marginal deposits characterised by features like low-angle thrust faulting, steeply dipping, and folded strata. This limitation leads to potential inaccuracies in resource estimation and mine planning, hindering the viability of these challenging resources. This paper advocates a return to fundamental principles, prioritising the application of 3D trigonometric calculations to determine true thickness. By incorporating factors such as seam topography, bedding plane orientation, and borehole deviation, this approach provides a robust foundation for subsequent modelling steps, including robust interpolation techniques like Radial Basis Functions, to generate continuous surfaces. This enhanced methodology, leveraging modern computing capabilities, offers improved accuracy and precision in stratigraphic mapping, crucial for unlocking resources at the margins of the Bowen Basin. The resulting high-precision operational planning model reduces the reliance on short-term planning adjustments, thereby enhancing mine planning efficiency. With ongoing data acquisition enabling continuous model refinement, our approach establishes a more reliable and enduring geological framework from the start.

1 Introduction
==============

Accurate stratigraphic modelling in the Bowen Basin's complex geological settings, particularly with steeply dipping and folded strata, poses challenges for traditional methodologies. Approaches like Independent Surfaces or Stacking often struggle to determine true stratigraphic thickness accurately in these environments, leading to potential model inaccuracies. This paper presents an innovative approach that prioritises 3D trigonometric calculations for precise true thickness determination, by accounting for surface topography, bedding orientation (dip), and borehole deviation. Subsequent interpolation, using techniques like Radial Basis Functions (RBFs), then creates continuous surfaces. Our enhanced methodology, leveraging modern computing, represents a technological step forward, offering improved accuracy for resource management in the Bowen Basin.

2 Challenges in Stratigraphic Modelling
=======================================

2.1 Defining True Thickness
---------------------------

Accurate stratigraphic modelling fundamentally relies on understanding true stratigraphic thickness. True thickness is defined as the perpendicular distance between the roof and floor of a stratigraphic unit. Its accurate determination is paramount, particularly in geologically complex scenarios, as this value is crucial for reliable resource estimation, mine planning, and production forecasting.

2.2 Traditional Method Limits
-----------------------------

Parts of the Bowen Basin are characterised by complex geological features that present substantial challenges to accurately modelling the true stratigraphic thickness defined above. These complexities include steeply dipping strata, folding, and faulting, which deviate significantly from the simpler geological settings assumed by many traditional modelling techniques (Saunders 1990). In such settings with steeply dipping strata, for instance, the apparent thickness, measured vertically, can significantly over or underestimate the actual volume of coal present. Similarly, folding can introduce rapid changes in dip and thickness over short distances, further complicating thickness calculations. Faulting adds another layer of complexity by creating discontinuities and offsets in the coal seams, requiring precise modelling to avoid errors in resource assessment and mine design.

2.3 Review of Old Methods
-------------------------

Traditional stratigraphic modelling methods often fall short in addressing these challenges effectively. Two common approaches are the Independent Surfaces method and the Stacking method.

### 2.3.1 Critique: Independent Surfaces\
Modelling seam roof and floor as independent surfaces often leads to inconsistencies in seam thickness and position, particularly in geologically complex areas requiring numerous, difficult-to-manage control strings or "phantom holes". Calculating thickness as the difference between two separate subjectively generated surfaces (as illustrated in Figure 1) can introduce significant inaccuracies, failing to honour the true geometric relationship between the surfaces.

Figure 1:  Cross section comparison of structural surfaces generated with traditional modelling techniques can be highly subjective.

### 2.3.2 Critique: Stacking Method\
The Stacking method, which applies thickness grids to a reference surface, also struggles to accurately represent true stratigraphic thickness. This is especially problematic in areas with dipping strata and non-vertical boreholes (demonstrated in Figure 2), as the method can prioritise control string conformity or smoothing over precise, geometrically sound thickness calculations derived from borehole data.

Figure 2:  Exploration drill strings tend to "wedge off" and deviate to intersect the sandstone/coal beds perpendicularly. Syncline and anticline structures can be subjectively interpreted and estimated from this deviation. Exploration holes are never perpendicular to a perfectly horizontal layer of coal.  (adapted from Heckscher et al., 2024)

In summary, the Bowen Basin's complex geology (including steeply dipping strata, folding, faulting, and borehole deviation), coupled with the deficiencies of traditional modelling methods---such as in handling control data, addressing data sparsity, and accurately determining true stratigraphic thickness---demands more robust techniques. Reliable resource management thus requires methodologies that integrate diverse data and employ geometrically sound calculations.

3 3D Trigonometric Calculation of True Thickness
================================================

3.1 Trigonometric Principles
----------------------------

A core innovation in addressing the limitations of traditional methods is the application of 3D trigonometric calculations to accurately determine true stratigraphic thickness. While the underlying principles draw upon fundamental geometric concepts (such as those of Pythagoras), their systematic application within a coal resource estimation workflow, as outlined in this paper, represents an advancement in the discipline. These calculations provide a more robust and accurate representation of seam thickness, especially in complex geological settings where traditional methods often fail. 

3.2 Principles and Formulation
------------------------------

Our methodology employs geometric principles and trigonometric functions to account for several critical factors that significantly influence thickness calculations:

- Structural Complexity of the Seam: In structurally complex deposits, coal seams exhibit significant variations in their elevation (RL) due to folding and faulting. Understanding and quantifying this complex 3D geometry, particularly the local bedding plane orientation (dip and strike) at any given point, is the primary challenge and is essential for accurate thickness calculations.

- Bedding plane orientation (dip): The dip angle of the coal seam is a primary control on the difference between apparent and true thickness. Trigonometry is used to resolve this difference, calculating the true thickness perpendicular to the dipping strata.

- Borehole deviation: In most cases, boreholes are not perfectly vertical. The deviation of the borehole trajectory must be considered to accurately calculate the true thickness intersected by the borehole.

By systematically incorporating these geometric realities, this trigonometric approach directly addresses inherent limitations in traditional methods. For instance, unlike the Independent Surfaces method, which calculates thickness from two independently modelled surfaces and can thus introduce inaccuracies, our new trigonometric method provides a direct and geometrically sound calculation of true thickness.\
Crucially, while geological interpretation remains vital for placing structural controls in data-sparse re\
gions, our trigonometric approach significantly reduces subjectivity in thickness determination itself by relying on direct calculation from observed data and interpreted structural orientations, rather than estimated thickness assignments for interpretive points. This inherently reduces inconsistencies and improves accuracy, particularly in areas with complex folding and rapid changes in dip. Similarly, in contrast to the Stacking method, which can struggle to represent true thickness accurately due to its reliance on smoothing and control strings rather than precise geometry, our                        trigonometric method explicitly incorporates the geometric relationship between the seam, borehole, and complex geology. The result is a more accurate and reliable representation of the coal seam's thickness distribution.

3.3 Governing Equations
-----------------------

The trigonometric calculations are based on established geometric principles. These principles allow for the resolution of distances and orientations in three-dimensional space, which is essential when dealing with dipping strata, deviated boreholes, and varying surface elevations.

A foundational illustration of these principles is provided by Dennison (1968), particularly for calculating true thickness (t) from measurements made on surface exposures where the slope of the local topography (α) is a direct factor. As shown in Figures 3 and 4 (adapted from Dennison, 1968), these calculations are:

Bedding dip (δ) is greater than topography dip (α):

                                                                              (1)

Bedding dip (δ) is less than topography dip (α):

                                                                                              (2)

Where: = horizontal distance between intersection points on the surface exposure; = angle between horizontal and topographic surface; = angle between horizontal & bedding plane (dip);  = vertical distance between intersection points.

Our proposed methodology rigorously applies these fundamental trigonometric principles, adapting them for subsurface borehole intercepts by utilising their 3D coordinates and local bedding orientation. This systematic, computationally-assisted determination of true thickness at each data point provides a more accurate and reliable foundation for subsequent stratigraphic modelling, leading to improved resource estimation and mine planning outcomes.

Figure 3: Bedding is greater than the dip of the topography.

Figure 4: Bedding is less than the dip of the topography.

4 Modelling Workflow
====================

Our proposed stratigraphic modelling methodology comprises a systematic workflow that prioritises accurate thickness determination before surface interpolation. This workflow integrates data processing, rigorous trigonometric calculations, interpolation, and model generation to create more accurate and reliable representations of coal seams, particularly in complex geological settings. The key steps involved are:

1. Establish a Structural Reference Surface: Create a primary structural surface (typically the roof of the uppermost ply for the seam group of interest) using available geological data and interpretation. This surface serves as the geometric foundation for subsequent calculations.

2. Calculate True Thickness Points: Determine the true stratigraphic thickness at empirically observed roof/floor point pairs. This involves applying the 3D trigonometric calculations detailed previously (Section 3.3), using data from sources like exploration drilling (accounting for deviation), in-situ survey pickups, and geophysically logged drill & blast holes. This step is crucial for accurately capturing thickness independent of structural dip or borehole orientation.

3. Interpolate a True Thickness Surface: Model a smooth, continuous true thickness grid surface across the deposit by interpolating the scattered true thickness points calculated in the previous step. RBFs are recommended for this interpolation due to their ability to honour data points and create geologically plausible surfaces without the artefacts (e.g., "bullseyes") associated with legacy methods like Inverse Distance Weighting (IDW), which should be considered deprecated.

4. Convert to Apparent Vertical Thickness: Transform the true thickness grid into an apparent vertical thickness grid. This involves calculating the vertical thickness component at each grid node, considering the local dip derived from the reference surface.

5. Generate Final Seam Surfaces: Subtract the apparent vertical thickness grid from the structural roof reference surface to generate the corresponding floor surface. If modelling multiple seams, this process can be repeated, using the floor of the upper seam as the reference surface for the seam below it.

Modern computing power, readily accessible through software environments like Python, plays a vital role in facilitating the efficient execution of the trigonometric equations and RBF interpolation required in this workflow (Heckscher et al. 2024), as well as managing the large geological datasets involved. Our structured approach, grounded in geometric principles, provides a robust framework for generating enhanced stratigraphic models.

5 Benefits and Implications
===========================

The improved stratigraphic modelling approach, incorporating 3D trigonometric calculations, offers several significant benefits and has important implications for coal mining operations, particularly in the more geologically complex parts of the Bowen Basin.

(1) Enhanced accuracy and precision increasing the overall confidence of resource estimation: By more accurately determining true stratigraphic thickness, our methodology leads to improved resource estimation. This is crucial for effective mine planning and financial forecasting, reducing the risk of over or underestimation of coal reserves.

(2) Better reconciliation between models and actual production: The more accurate models generated by this approach result in better reconciliation between predicted coal volumes and actual production figures. This improved agreement allows for more reliable production schedules and reduces discrepancies that can lead to operational inefficiencies.

(3) Optimised mine planning and production forecasting: Accurate resource models are essential for effective mine planning and production forecasting. The enhanced precision offered by our methodology enables the development of more realistic mine plans, optimised extraction sequences, and more reliable predictions of future production levels.

(4) Support for more efficient and sustainable resource extraction: Ultimately, the improved accuracy and precision of stratigraphic modelling contribute to more efficient and sustainable resource extraction. By reducing uncertainties and improving decision-making, our approach helps to minimise waste, optimise resource recovery, and promote responsible mining practices.

(5) Our methodology represents a technological innovation in stratigraphic modelling, directly addressing the challenges posed by complex geological settings in parts of the Bowen Basin. Its focus on accurate true thickness determination and integration with modern computing aligns with the symposium's "Technology and Innovation" theme, offering a pathway to enhanced efficiency and sustainability in the coal industry.

6 Conclusion
============

This paper has presented a refined stratigraphic modelling methodology tailored for the complex geology found in parts of the Bowen Basin. Its core strength is the emphasis on accurately determining true stratigraphic thickness using 3D trigonometric calculations. By incorporating surface topography, bedding orientation, and borehole deviation, our method addresses limitations inherent in traditional techniques when applied to structurally complex strata. The subsequent integration of these precise calculations with robust interpolation methods, like RBFs, facilitated by modern computing, yields enhanced stratigraphic models. This leads to more accurate resource estimation, improved reconciliation, and optimised mine planning, thereby supporting more efficient and sustainable resource extraction.

7 References
============

Dennison, J. M. (1968). Analysis of geologic structures. W. W. Norton & Company.

Heckscher, N. J., Hughes, A. Saunders, B. J., Owen, G. (2024). Beyond Traditional Methods: Radial Basis Functions for Stratigraphic Modelling Innovation in Complex Coal Deposits. Proceedings of the 2024 Sydney Basin Symposium.

Saunders, B. J. (1990). The use of Dipmeters for structural assessment in coal mine development. In A. R. G. Gray & J. A. Salomon (Eds.), Bowen Basin Symposium 1990: Proceedings (pp. 153-155). Geological Society of Australia, Queensland Division.
