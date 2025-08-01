# oscillating-pareto
Hybrid Severity/Pricing Curve with Scaled Oscillatory-Adjusted Pareto Inverse CDF

This repository contains a custom hybrid pricing/severity model based on the inverse Pareto CDF with an added oscillatory component using cosine functions.

The model introduces scalable, dampened oscillations to allow flexible pricing behavior across percentiles, suitable for insurance, actuarial modeling, and advanced pricing strategies.

## Formula (simplified):
### form-1
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · cos(fp + φ) · e^(-kp) · p^β + δ ]
### form-2
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · sin(fp + φ) · e^(-kp) · p^β + δ ]
### form-3
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · sin(π * fp + φ) · e^(-kp) · p^β + δ ]
### form-4
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · cos(π * fp + φ) · e^(-kp) · p^β + δ ]
### form-5
F(p) = λ(1−p)−α +A(1−p)β sin(fp+ϕ)+δ
ex.
F(p)= $E$7 + ($E$2 / (1 - F9)^($E$1)) + $E$4 * (1 - F9)^$E$6 * SIN($E$5 * F9 + $E$3)
### simplest-form-1
F(p)=λ*(1-p)^(-α)+A*p^β*sin(f*p)

Where:
- `p` = percentile
- `S` = scaling
- `α`, `λ` = Pareto parameters
- `A`, `f`, `φ`, `k`, `β`, `δ` = oscillation controls


## License

Proprietary – All Rights Reserved  
© Yosef Yaakov Bunick 7/25/2025  

##Intellectual Property Notice

This model — including its formulas, structure, and supporting files — is the intellectual property of Yosef Yaakov Bunick.
No part of this work may be copied, reproduced, distributed, or used in any form without the explicit written permission of the author.
Unauthorized use, reproduction, or modification of this content is strictly prohibited and may result in legal action.
This model may not be copied, reused for commercial purposes, or distributed without proper attribution and prior permission.

## License for shared use
CC BY-SA 4.0 ©
The *Formula Only* is licensed under the Attribution-ShareAlike 4.0 International. https://creativecommons.org/licenses/by-sa/4.0/

Attribution — You must give appropriate credit , provide a link to the license, and indicate if changes were made.

ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

This Creative Commons license applies **only to the formula as shared**, and **not to the full model, its structure, or supporting files**, which remain fully proprietary and protected under copyright.
