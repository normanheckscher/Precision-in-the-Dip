# Precision in the dip: true thickness calculation for complex coal deposits

N.J. Heckscher & B.J. Saunders

QEGSS Pty Ltd, Moranbah, Australia

ABSTRACT: Stratigraphic modelling within the Bowen Basin is frequently simplified by focusing on large-scale, economically dominant deposits where traditional methods, such as Independent Surfaces and Stacking, prove adequate. However, these methods fail in structurally complex areas with steeply dipping and folded strata, leading to inaccurate resource estimation and hindering the viability of these challenging resources. This paper presents a refined methodology that applies 3D trigonometric calculations to determine true thickness with greater precision. By incorporating factors like seam topography, bedding plane orientation, and borehole deviation, our approach provides a robust foundation for subsequent interpolation using techniques like Radial Basis Functions. The resulting high-precision operational model enhances mine planning efficiency and establishes a more reliable geological framework from the start.

# INTRODUCTION

Accurate stratigraphic modelling in the Bowen Basin's complex geological settings, particularly with steeply dipping and folded strata, poses challenges for traditional methodologies. Approaches like Independent Surfaces or Stacking often struggle to determine true stratigraphic thickness accurately in these environments, leading to potential model inaccuracies. This paper presents an innovative approach that prioritises 3D trigonometric calculations for precise true thickness determination, by accounting for surface topography, bedding orientation (dip), and borehole deviation. Subsequent interpolation, using techniques like Radial Basis Functions (RBFs), then creates continuous surfaces. Our enhanced methodology, leveraging modern computing, represents a technological step forward, offering improved accuracy for resource management in the Bowen Basin.

# CHALLENGES IN STRATIGRAPHIC MODELLING

## Defining true thickness

Accurate stratigraphic modelling fundamentally relies on understanding true stratigraphic thickness. True thickness is defined as the perpendicular distance between the roof and floor of a stratigraphic unit. Its accurate determination is paramount, particularly in geologically complex scenarios, as this value is crucial for reliable resource estimation, mine planning, and production forecasting.

## Traditional method limits

Parts of the Bowen Basin are characterised by complex geological features that present substantial challenges to accurately modelling the true stratigraphic thickness defined above. These complexities include steeply dipping strata, folding, and faulting, which deviate significantly from the simpler geological settings assumed by many traditional modelling techniques (Saunders 1990). In such settings with steeply dipping strata, for instance, the apparent thickness, measured vertically, can significantly over or underestimate the actual volume of coal present. Similarly, folding can introduce rapid changes in dip and thickness over short distances, further complicating thickness calculations. Faulting adds another layer of complexity by creating discontinuities and offsets in the coal seams, requiring precise modelling to avoid errors in resource assessment and mine design.

## Review of old methods

Traditional stratigraphic modelling methods often fall short in addressing these challenges effectively (Barber & Whyte 2015). Two common approaches are the Independent Surfaces method and the Stacking method.

### Critique: independent surfaces

Modelling seam roof and floor as independent surfaces often leads to inconsistencies in seam thickness and position, particularly in geologically complex areas requiring numerous, difficult-to-manage control strings or "phantom holes". Calculating thickness as the difference between two separate subjectively generated surfaces (as illustrated in Figure 1) can introduce significant inaccuracies, failing to honour the true geometric relationship between the surfaces.

<img width="533" height="218" alt="image" src="https://github.com/user-attachments/assets/fca6b54d-0390-41e9-bf84-df13225e89c1" />

Figure 1. A conceptual cross-section illustrating how independently modelled roof and floor surfaces (dotted lines) based on drillhole intercepts (black vertical bars) can lead to subjective and inconsistent thickness interpretations (red crosses).

### Critique: stacking method

The Stacking method, which applies thickness grids to a reference surface, also struggles to accurately represent true stratigraphic thickness. This is especially problematic in areas with dipping strata and non-vertical boreholes (demonstrated in Figure 2), as the method can prioritise control string conformity or smoothing over precise, geometrically sound thickness calculations derived from borehole data.


Figure 2. An example of steeply dipping and folded seams (upper and lower surfaces) with deviated drillhole paths (dashed white lines), demonstrating complex geometries where traditional methods may fail. (adapted from Heckscher et al., 2024)

In summary, the Bowen Basin's complex geology (including steeply dipping strata, folding, faulting, and borehole deviation), coupled with the deficiencies of traditional modelling methods-such as in handling control data, addressing data sparsity, and accurately determining true stratigraphic thickness-demands more robust techniques. Reliable resource management thus requires methodologies that integrate diverse data and employ geometrically sound calculations.

# 3D TRIGONOMETRIC CALCULATION OF TRUE THICKNESS

## Trigonometric principles

A core innovation in addressing the limitations of traditional methods is the application of 3D trigonometric calculations to accurately determine true stratigraphic thickness. While the underlying principles draw upon fundamental geometric concepts (such as those of Pythagoras), their systematic application within a coal resource estimation workflow, as outlined in this paper, represents an advancement in the discipline. These calculations provide a more robust and accurate representation of seam thickness, especially in complex geological settings where traditional methods often fail.

## Principles and formulation

Our methodology employs geometric principles and trigonometric functions to account for several critical factors that significantly influence thickness calculations:

- Structural Complexity of the Seam: In structurally complex deposits, coal seams exhibit significant variations in their elevation (RL) due to folding and faulting. Understanding and quantifying this complex 3D geometry, particularly the local bedding plane orientation (dip and strike) at any given point, is the primary challenge and is essential for accurate thickness calculations.
- Bedding plane orientation (dip, δ): The dip angle of the coal seam is a primary control on the difference between apparent and true thickness. Trigonometry is used to resolve this difference, calculating the true thickness perpendicular to the dipping strata.
- Borehole deviation: In most cases, boreholes are not perfectly vertical. The deviation of the borehole trajectory must be considered to accurately calculate the true thickness intersected by the borehole. This requires accounting for the differences in the X, Y, and Z coordinates (_ΔX, ΔY, ΔZ_) between the roof and floor intercepts, the plan view length of the drillhole path (), and the angle (β) between the drillhole's horizontal bearing and the local dip direction of the strata. The drillhole's horizontal bearing is determined from its intercepts (_ΔX, ΔY_) using the four-quadrant arctan2 function.

By systematically incorporating these geometric realities, this trigonometric approach directly addresses inherent limitations in traditional methods. For instance, unlike the Independent Surfaces method, which calculates thickness from two independently modelled surfaces and can thus introduce inaccuracies, our new trigonometric method provides a direct and geometrically sound calculation of true thickness. Crucially, while geological interpretation remains vital for placing structural controls in data sparse regions, our trigonometric approach significantly reduces subjectivity in thickness determination itself by relying on direct calculation from observed data and interpreted structural orientations, rather than estimated thickness assignments for interpretive points. This inherently reduces inconsistencies and improves accuracy, particularly in areas with complex folding and rapid changes in dip. Similarly, in contrast to the Stacking method, which can struggle to represent true thickness accurately due to its reliance on smoothing and control strings rather than precise geometry, our trigonometric method explicitly incorporates the geometric relationship between the seam, borehole, and complex geology. The result is a more accurate and reliable representation of the coal seam's thickness distribution.

## Governing equations

The calculations use established geometric principles to resolve distances and orientations in three-dimensional space. A foundational illustration of these principles for surface exposures is provided by Dennison (1968). For measurements taken on a surface exposure, the true thickness (t) can be determined from the outcrop's horizontal distance (h), the vertical elevation change (v), the topographic slope (α), and the bedding dip (δ). The method uses a conditional approach based on the relationship between the bedding dip and the topographic slope.

Bedding dip (δ) is greater than topographic slope (α):

t = |h cos α sin δ - v cos δ|  							(1)

Bedding dip (δ) is less than topographic slope (α):

t = h cos α sin δ + v cos δ								(2)

Our methodology adapts and extends these principles for 3D subsurface drillhole intercepts. This also requires a conditional approach to robustly handle both normal and overturned strata, based on the sign of _ΔZ_ (the vertical difference between the roof and floor intercepts).

For a standard intercept where the roof is at a higher elevation than the floor, the true thickness is calculated as:

t = |h ⋅cos β ⋅sin δ - ΔZ⋅ cos δ|					(3)

For an overturned intercept where the roof is below the floor, the formula is adjusted to:

t = |h ⋅cos β ⋅sin δ+ ΔZ⋅ cos δ|					(4)

Our proposed methodology rigorously applies these fundamental trigonometric principles, adapting them for subsurface borehole intercepts by utilising their 3D coordinates and local bedding orientation. This systematic, computationally-assisted determination of true thickness at each data point provides a more accurate and reliable foundation for subsequent stratigraphic modelling, leading to improved resource estimation and mine planning outcomes.

<img width="429" height="299" alt="image" src="https://github.com/user-attachments/assets/d6fc7e79-a6c3-4ccd-904b-47095bf0fd6b" />

Figure 3. Geometry where bedding dip (δ) is greater than topographic slope (α), showing horizontal distance h (segment ab) and vertical distance v (segment bc). (adapted Dennison 1968).

<img width="412" height="321" alt="image" src="https://github.com/user-attachments/assets/60d55224-856f-423a-8e0c-dfd60b000eaa" />

Figure 4. Geometry where bedding dip (δ) is less than topographic slope (α), showing horizontal distance h (segment ab) and vertical distance v (segment bc). (adapted Dennison 1968).

# MODELLING WORKFLOW

Our proposed stratigraphic modelling methodology comprises a systematic workflow that prioritises accurate thickness determination before surface interpolation. This workflow integrates data processing, rigorous trigonometric calculations, interpolation, and model generation to create more accurate and reliable representations of coal seams, particularly in complex geological settings. The key steps involved are:

1) Establish a Structural Reference Surface: Create a primary structural surface (e.g., the uppermost ply roof) from geological data to serve as the geometric foundation for all subsequent calculations.
2) Calculate True Thickness Points: Determine the true stratigraphic thickness at empirically observed roof/floor point pairs. This involves applying the 3D trigonometric calculations detailed previously (Section 3.3), using data from sources like exploration drilling (accounting for deviation), in-situ survey pickups, and geophysically logged drill & blast holes. This step captures thickness independent of structural dip or borehole orientation.
3) Interpolate a True Thickness Surface: Interpolate the scattered true thickness points into a continuous grid. Radial Basis Functions (RBFs) are recommended over deprecated methods like IDW to create a smooth surface that accurately honours the data. Furthermore, the use of IDW has been questioned as it is an inherently conservative technique that relies on an arbitrary weighting power and cannot produce estimates outside the range of the source data (Waltho et al. 2014).
4) Convert to Apparent Vertical Thickness: Transform the true thickness grid into an apparent vertical thickness grid. This involves calculating the vertical thickness component at each grid node, considering the local dip derived from the reference surface.
5) Generate Final Seam Surfaces: Subtract the apparent vertical thickness grid from the structural roof reference surface to generate the corresponding floor surface. If modelling multiple seams, this process can be repeated, using the floor of the upper seam as the reference surface for the seam below it.

Modern computing power, readily accessible through software environments like Python plays a vital role in facilitating the efficient execution of the trigonometric equations and RBF interpolation required in this workflow (Heckscher et al. 2024), as well as managing the large geological datasets involved. Our structured approach, grounded in geometric principles, provides a robust framework for generating enhanced stratigraphic models.

# BENEFITS AND IMPLICATIONS

The improved stratigraphic modelling approach, incorporating 3D trigonometric calculations, offers several significant benefits and has important implications for coal mining operations, particularly in the more geologically complex parts of the Bowen Basin.

Enhanced accuracy and precision increasing the overall confidence of resource estimation: By more accurately determining true stratigraphic thickness, our methodology leads to improved resource estimation. This reduces financial risk and is crucial for effective mine planning.

Better reconciliation between models and actual production: The more accurate models generated by this approach result in better reconciliation between predicted coal volumes and actual production figures. This improved agreement allows for more reliable production schedules and reduces discrepancies that can lead to operational inefficiencies.

Optimised mine planning and production forecasting: Accurate resource models are essential for effective mine planning and production forecasting. The enhanced precision offered by our methodology enables the development of more realistic mine plans, optimised extraction sequences, and more reliable predictions of future production levels.

Support for more efficient and sustainable resource extraction: Ultimately, the improved accuracy and precision of stratigraphic modelling contribute to more efficient and sustainable resource extraction. By reducing uncertainties and improving decision-making, our approach helps to minimise waste, optimise resource recovery, and promote responsible mining practices.

Our methodology represents a technological innovation in stratigraphic modelling, directly addressing the challenges posed by complex geological settings in parts of the Bowen Basin. Its focus on accurate true thickness determination and integration with modern computing aligns with the symposium's "Technology and Innovation" theme, offering a pathway to enhanced efficiency and sustainability in the coal industry.

# CONCLUSION

This paper has presented a refined stratigraphic modelling methodology tailored for the complex geology found in parts of the Bowen Basin. Its core strength is the emphasis on accurately determining true stratigraphic thickness using 3D trigonometric calculations. By incorporating surface topography, bedding orientation, and borehole deviation, our method addresses limitations inherent in traditional techniques when applied to structurally complex strata. Integrating these precise calculations with robust interpolation (like RBFs) yields enhanced models. This leads to more accurate resource estimation, improved reconciliation, and optimised mine planning, supporting more sustainable resource extraction.

# REFERENCES

Barber, J. & Whyte, S. 2015. The influence of drill hole deviation on resource estimates in steep dip deposits. _AusIMM Bulletin_ (Dec 2015): 48-51.

Dennison, J. M. 1968. _Analysis of geologic structures_. New York: W. W. Norton & Company.

Heckscher, N. J., Hughes, A. Saunders, B. J., Owen, G. 2024. Beyond Traditional Methods: Radial Basis Functions for Stratigraphic Modelling Innovation in Complex Coal Deposits. _Proceedings of the 2024 Sydney Basin Symposium_.

Saunders, B. J. 1990. The use of Dipmeters for structural assessment in coal mine development. In A. R. G. Gray & J. A. Salomon (Eds.), _Bowen Basin Symposium 1990_: Proceedings (pp. 153-155). Geological Society of Australia, Queensland Division.

Waltho, A., Kristensen, S. & Harman, C. (2014). Best Practice in Coal Exploration and Resource Evaluation. In: _Mineral Resource and Ore Reserve Estimation: The AusIMM Guide to Good Practice_ (Second edition), Monograph 30, pp. 155-174 (The Australasian Institute of Mining and Metallurgy: Carlton, VIC).
