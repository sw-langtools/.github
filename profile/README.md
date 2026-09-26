## sw-langtools — the compiler machinery the emulators share

The reusable parts, factored out once more than one machine needed them: a target-independent SSA representation with an optimizer, and shared ISA, code-generation and target cores. A RISC-V RV32I toolchain is built on them as the worked example.

**10 repositories** of my own.

| Repository | What it is |
|---|---|
| [sw-rv32i-asm](https://github.com/sw-langtools/sw-rv32i-asm) | RV32I Assembler: text source to instruction bytes |
| [sw-rv32i-target](https://github.com/sw-langtools/sw-rv32i-target) | RV32I Target description: ABI, calling convention, register classes |
| [sw-rv32i-emulator](https://github.com/sw-langtools/sw-rv32i-emulator) | RV32I Emulator: instruction execution semantics |
| [sw-rv32i-isa](https://github.com/sw-langtools/sw-rv32i-isa) | RV32I ISA description: opcodes, encoding, decoding, disassembly |
| [sw-rv32i-codegen](https://github.com/sw-langtools/sw-rv32i-codegen) | RV32I Codegen: lowering TIR to instructions |
| [sw-codegen-core](https://github.com/sw-langtools/sw-codegen-core) | Codegen scaffolding (regalloc, branch relaxation, frame, asm) for the sw-langtools toolchain |
| [sw-tir-opt](https://github.com/sw-langtools/sw-tir-opt) | Target-independent TIR optimisation passes for the sw-langtools toolchain |
| [sw-tir](https://github.com/sw-langtools/sw-tir) | Target-Independent Representation (TIR): SSA IR with block parameters for the sw-langtools toolchain |

If an emulator elsewhere in these organizations can assemble, optimize or generate code, this is usually where that part lives.

**→ [The index](https://github.com/softwarewrighter/softwarewrighter)** — all 251 public repositories across 15 accounts, grouped by topic, with the map of which are worth your ten minutes.
