# oscillating-pareto
Hybrid Severity/Pricing Curve with Scaled Oscillatory-Adjusted Pareto Inverse CDF

This repository contains a custom hybrid pricing/severity model based on the inverse Pareto CDF with an added oscillatory component using cosine functions.

The model introduces scalable, dampened oscillations to allow flexible pricing behavior across percentiles, suitable for insurance, actuarial modeling, and advanced pricing strategies.

## Formula (simplified):

F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · cos(fp + φ) · e^(-kp) · p^β + δ ]
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · sin(fp + φ) · e^(-kp) · p^β + δ ]
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · sin(π * fp + φ) · e^(-kp) · p^β + δ ]
F(p) = S · [ λ((1 - p)^(-1/α) - 1) + trunc + V + A · cos(π * fp + φ) · e^(-kp) · p^β + δ ]
Where:
- `p` = percentile
- `S` = scaling
- `α`, `λ` = Pareto parameters
- `A`, `f`, `φ`, `k`, `β`, `δ` = oscillation controls



## License

Proprietary – All Rights Reserved  
© Yosef Yaakov Bunick 7/25/2025  

This model, including its formulas, structure, and supporting files, is the intellectual property of Yosef Yaakov Bunick.  
No part of this work may be copied, reproduced, distributed, or used in any form without explicit written permission from the author.
Unauthorized use, reproduction, or modification of this content is prohibited and may result in legal action.
This model may not be copied, reused, or distributed without permission.
