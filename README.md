# 1H–15N BB-HSQC

The 1H–15N BB-HSQC (Broadband Heteronuclear Single Quantum Coherence) experiment is designed for detecting 1H-15N correlations in biomolecules and metabolites. This experiment utilizes novel AI-designed broadband 15N universal 180° pulses for both inversion and refocusing operations, significantly enhancing spectral sensitivity across the full range of 15N chemical shifts. This capability is especially valuable at high and ultra-high magnetic fields for the identification and quantification of nitrogen-containing metabolites such as amides, amines, and imines in biological fluids and cell extracts.

---
## Files
| File Name                             | Type                  | Description                       |
| ------------------------------------- | --------------------- | --------------------------------- |
| `bbhsqcetf3gpsi2.3`                  | Bruker Pulse Sequence | 2D 1H–15N broadband HSQC with sensitivity improvement |
| `pix_rf0.00_24.200p1_bw1.40p1.mrf`   | RF Shape              | AI-designed 15N universal 180° pulse for inversion/refocusing |
| `z2iz_rf0.00_10.021p1_bw2.40B1.mrf`  | RF Shape              | 13C inversion pulse for decoupling |

---
## Experimental Setup

### 1H–15N BB-HSQC
- **Pulse Sequence:**  
   `bbhsqcetf3gpsi2.3` - 2D H-1/X correlation via double inept transfer 
- **RF Shapes:**  
  - `pix_rf0.00_24.200p1_bw1.40p1.mrf` (15N   π-pulse for inversion/refocusing)  
  - `z2iz_rf0.00_10.021p1_bw2.40B1.mrf` (13C inversion pulse for decoupling)
- **Pulse Parameters:**
  - `p57 = p21*24.20`  
  - `spoff57 = 0.0`  
  - `spw57 = plw3`  
  - `p56 = p3*10.021`  
  - `spw56 = plw2`  
  - `spoff56 = 0.0`  
- **Gradient Settings:**  
  - `gpz0`: -2%
  - `gpz1`: -61%
  - `gpz2`: 80%
  - `gpz3`: 8.1% (for N-15)
  - `gpz4`: 11%
  - `gpz5`: 17%
  - `gpz6`: 23%
  - Gradient shape names set to `SMSQ10.100` for all gradient pulses


  - **Note:** For optimal performance with metabolite samples, adjust water suppression parameters and INEPT transfer delays based on the specific sample conditions.

---
Copyright & License Statement

RF pulse shapes are copyrighted by Regents of the University of Minnesota and the software for generating RF shapes covered by US patent 11,221,384. Regents of the University of Minnesota will license the use of RF shapes solely for educational and research purposes by non-profit institutions and government agencies only. For other proposed uses, contact umotc@umn.edu. The software may not be sold or redistributed without prior approval. One may make copies of the software for their use provided that the copies, are not sold or distributed, are used under the same terms and conditions. As unestablished research software, this code is provided on an "as is'' basis without warranty of any kind, either expressed or implied. The downloading, or executing any part of this software constitutes an implicit agreement to these terms. These terms and conditions are subject to change at any time without prior notice.
