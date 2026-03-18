# Annexure A: Band Value Behaviour

The tables below describe how a band’s intrinsic and extrinsic value change as perp mark price moves relative to the band’s inner and outer bounds.

### Long Band

For long bands, inner bound < outer bound. Intrinsic value is capped at outer − inner when fully ITM.

| **Range Status**                      | **Price Move** | **Updated Range Status** | **Intrinsic Value**            | **Extrinsic Value**           |
| ------------------------------------- | -------------- | ------------------------ | ------------------------------ | ----------------------------- |
| **price < inner < outer (OTM)**       | up             | —                        | 0 (still OTM)                  | ↑ price closer to inner       |
| <p><br></p>                           | down           | —                        | 0 (still OTM)                  | ↓ price further from inner    |
| <p><br></p>                           | —              | inner < price < outer    | ↑ becomes nonzero              | ↓ intrinsic absorbs extrinsic |
| **inner < price < outer (in range)**  | up             | —                        | ↑ price further from inner     | ↓ price closer to outer       |
| <p><br></p>                           | down           | —                        | ↓ price closer to inner        | ↑ price further from outer    |
| <p><br></p>                           | —              | price < inner < outer    | ↓ to 0, exits range past inner | ↑ then ↓ peaks near inner     |
| <p><br></p>                           | —              | inner < outer < price    | ↑ capped at outer−inner        | ↓ to 0 (fully ITM)            |
| **inner < outer < price (fully ITM)** | up             | —                        | capped (unchanged)             | 0 (still fully ITM)           |
| <p><br></p>                           | down           | —                        | capped (unchanged)             | 0 (still fully ITM)           |
| <p><br></p>                           | —              | inner < price < outer    | ↓ intrinsic uncaps             | ↑ extrinsic reappears         |

### Short Band

For short bands, inner bound > outer bound. Intrinsic value is capped at inner − outer when fully ITM.

| **Range Status**                      | **Price Move** | **Updated Range Status** | **Intrinsic Value**            | **Extrinsic Value**           |
| ------------------------------------- | -------------- | ------------------------ | ------------------------------ | ----------------------------- |
| **price > inner > outer (OTM)**       | up             | —                        | 0 (still OTM)                  | ↓ price further from inner    |
| <p><br></p>                           | down           | —                        | 0 (still OTM)                  | ↑ price closer to inner       |
| <p><br></p>                           | —              | inner > price > outer    | ↑ becomes nonzero              | ↓ intrinsic absorbs extrinsic |
| **inner > price > outer (in range)**  | up             | —                        | ↓ price closer to inner        | ↑ price further from outer    |
| <p><br></p>                           | down           | —                        | ↑ price further from inner     | ↓ price closer to outer       |
| <p><br></p>                           | —              | price > inner > outer    | ↓ to 0, exits range past inner | ↑ then ↓ peaks near inner     |
| <p><br></p>                           | —              | inner > outer > price    | ↑ capped at inner−outer        | ↓ to 0 (fully ITM)            |
| **inner > outer > price (fully ITM)** | up             | —                        | capped (unchanged)             | 0 (still fully ITM)           |
| <p><br></p>                           | down           | —                        | capped (unchanged)             | 0 (still fully ITM)           |
| <p><br></p>                           | —              | inner > price > outer    | ↓ intrinsic uncaps             | ↑ extrinsic reappears         |
