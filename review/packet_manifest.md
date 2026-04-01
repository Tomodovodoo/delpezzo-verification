# Packet Manifest

Source PDF: [delpezzo.pdf](E:\Personal\Random\Random\Delpezzo\delpezzo.pdf)

PDF page convention:

- Printed page `n` in the paper appears on PDF page `n+1`.
- The title page is PDF page `1`.

## Gates

- `G0`: terminology and citation ledger from `Sections 1-2` and references.
- `G1`: explicit-corridor review of `Sections 3-8`.
- `G2`: Route C entry packets `Section 9.3-Section 9.6`.
- `G3`: all of `Section 9`.
- `G4`: all of `Section 11`.
- `G5`: final theorem trace through `Section 10`, `Section 11.15`, and `Section 12.3`.

## Packets

### Pre-Section-9

| Packet | Scope | Printed pages | PDF pages | Depends on |
| --- | --- | --- | --- | --- |
| `P00` | cover, abstract, `Section 1`, `Section 1.1`, Table 1 context | 1-7 | 1-8 | none |
| `P01` | `Section 2` and terminology/citation ledger | 7 | 8 | `P00` |
| `P02` | `Section 3.1` | 8 | 9 | `G0` |
| `P03` | `Section 3.2` | 8-9 | 9-10 | `G0` |
| `P04` | `Section 4.1` | 9-10 | 10-11 | `G0` |
| `P05` | `Section 4.2` | 10-11 | 11-12 | `G0` |
| `P06` | `Section 5` | 11-12 | 12-13 | `G0` |
| `P07` | `Section 6.1-Section 6.2` | 12 | 13 | `G0` |
| `P08` | `Section 6.3-Section 6.5` | 13-14 | 14-15 | `G0` |
| `P09` | `Section 7.1-Section 7.3` | 14-17 | 15-18 | `G0` |
| `P10` | `Section 8.1-Section 8.5` | 17-19 | 18-20 | `G0` |
| `P11` | `Section 8.6-Section 8.8` | 19-22 | 20-23 | `P10` |

### Section 9

| Packet | Scope | Printed pages | PDF pages | Depends on |
| --- | --- | --- | --- | --- |
| `9A` | `Section 9.3` | 24-26 | 25-27 | `G1` |
| `9B` | `Section 9.4` | 26-27 | 27-28 | `9A` |
| `9C` | `Section 9.5a` | 27-30 | 28-31 | `9B` |
| `9D` | `Section 9.5b` | 30-33 | 31-34 | `9C` |
| `9E` | `Section 9.5c-Section 9.6` | 34-40 | 35-41 | `9D` |
| `9F` | `Section 9.7-Section 9.9` | 41-46 | 42-47 | `9E` |
| `9G` | `Section 9.10-Section 9.12` | 46-52 | 47-53 | `9F` |
| `9H` | `Section 9.13-Section 9.15` | 52-60 | 53-61 | `9G` |
| `9I` | `Section 9.16-Section 9.18` | 60-66 | 61-67 | `9H` |
| `9J` | `Section 9.19-Section 9.21` | 66-71 | 67-72 | `9I` |
| `9K` | `Section 9.22-Section 9.23` | 72-76 | 73-77 | `9J` |
| `9L` | `Section 9.23-Section 9.24a` | 76-80 | 77-81 | `9K` |
| `9M` | `Section 9.24b` | 80-84 | 81-85 | `9L` |
| `9N` | `Section 9.24c-Section 9.25` | 84-88 | 85-89 | `9M` |
| `9O` | `Section 9.25-Section 9.26a` | 88-95 | 89-96 | `9N` |
| `9P` | `Section 9.26a` | 95-97 | 96-98 | `9O` |
| `9Q` | `Section 9.26-Section 9.27` | 97-101 | 98-102 | `9P` |
| `9R` | `Section 9.28a` | 101-105 | 102-106 | `9Q` |
| `9S` | `Section 9.28b-Section 9.28c` | 105-110 | 106-111 | `9R` |
| `9T` | `Section 9.29` | 111-113 | 112-114 | `9S` |
| `9U` | `Section 9.30` | 113-116 | 114-117 | `9T` |

### Section 10

| Packet | Scope | Printed pages | PDF pages | Depends on |
| --- | --- | --- | --- | --- |
| `10A` | `Section 10` | 116 | 117 | `G3` |

### Section 11

| Packet | Scope | Printed pages | PDF pages | Depends on |
| --- | --- | --- | --- | --- |
| `11A` | `Section 11` prelude | 117-120 | 118-121 | `10A` |
| `11B` | remaining prelude | 120-124 | 121-125 | `11A` |
| `11C` | `Section 11.1` | 124-128 | 125-129 | `11B` |
| `11D` | `Section 11.2a` | 128-131 | 129-132 | `11C` |
| `11E` | `Section 11.2b` | 131-134 | 132-135 | `11D` |
| `11F` | `Section 11.3` | 135-137 | 136-138 | `11E` |
| `11G` | `Section 11.4-Section 11.5` | 137-143 | 138-144 | `11F` |
| `11H` | `Section 11.5-Section 11.6` | 143-146 | 144-147 | `11G` |
| `11I` | `Section 11.7` | 148-150 | 149-151 | `11H` |
| `11J` | `Section 11.8` | 151-154 | 152-155 | `11I` |
| `11K` | `Section 11.9-Section 11.10` | 155-161 | 156-162 | `11J` |
| `11L` | `Section 11.10-Section 11.12` | 161-168 | 162-169 | `11K` |
| `11M` | end `Section 11.12` + `Section 11.13a` | 168-171 | 169-172 | `11L` |
| `11N` | `Section 11.13b` | 171-176 | 172-177 | `11M` |
| `11O` | `Section 11.13c` | 176-179 | 177-180 | `11N` |
| `11P` | `Section 11.13d` | 179-183 | 180-184 | `11O` |
| `11Q` | `Section 11.13e-Section 11.13f` | 183-189 | 184-190 | `11P` |
| `11R` | end `Section 11.13f` + `Section 11.14` | 189-191 | 190-192 | `11Q` |
| `11S` | `Section 11.15` | 192-195 | 193-196 | `11R` |
| `11T` | section synthesis | 195-196 | 196-197 | `11S` |

### Section 12

| Packet | Scope | Printed pages | PDF pages | Depends on |
| --- | --- | --- | --- | --- |
| `12A` | prelude + `Section 12.1a` | 195-199 | 196-200 | `G4` |
| `12B` | end `Section 12.1a` + `Section 12.1b` | 199-201 | 200-202 | `12A` |
| `12C` | `Section 12.1b-Section 12.1c` | 201-206 | 202-207 | `12B` |
| `12D` | `Section 12.1c-Section 12.1d` | 206-208 | 207-209 | `12C` |
| `12E` | `Section 12.1e` | 208-210 | 209-211 | `12D` |
| `12F` | `Section 12.1f` | 211-214 | 212-215 | `12E` |
| `12G` | `Section 12.1g` | 214-216 | 215-217 | `12F` |
| `12H` | `Section 12.2a` | 216-219 | 217-220 | `12G` |
| `12I` | `Section 12.2b` | 219-222 | 220-223 | `12H` |
| `12J` | `Section 12.2c` | 222-224 | 223-225 | `12I` |
| `12K` | `Section 12.2d` | 224-227 | 225-228 | `12J` |
| `12L` | `Section 12.2e` | 227-229 | 228-230 | `12K` |
| `12M` | `Section 12.2f` | 229-231 | 230-232 | `12L` |
| `12N` | end `Section 12.2` + start `Section 12.3` | 231-234 | 232-235 | `12M` |
| `12O` | end `Section 12.3` and final closure | 234-235 | 235-236 | `12N`, `10A`, `11S` |
