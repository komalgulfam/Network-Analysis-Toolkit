# Subnet Mask & Block Size Calculation

## Calculation Methodology
When analyzing a subnet range such as `10.10.10.13/29`:
1. Convert the subnet mask binary notation: `11111111.11111111.11111111.11111000`
2. Examine the last octet term (`11111000`).
3. Calculate bit values ($1 + 2 + 4 + 8 + 16 + 32 + 64 + 128$). Since the first 3 bits are zeros, ignore them and sum the remaining active bits: $8 + 16 + 32 + 64 + 128 = 248$.
4. Subtract from 256 to find the block size: $256 - 248 = 8$.
5. Resulting block ranges: `0-7`, `8-15`, `16-23`, etc.
