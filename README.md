# symstrip

## Usage
* [dump .symtab]
```
ⵧ➤ sudo ./symstrip -f $HOME/shell -d

    File architecture: x86-64
     0: 0x0000000000000000   0      NOTYPE   LOCAL    DEFAULT  UND  
     1: 0x0000000000400238   0      SECTION  LOCAL    DEFAULT  1    
     2: 0x0000000000400254   0      SECTION  LOCAL    DEFAULT  2    
     3: 0x0000000000400274   0      SECTION  LOCAL    DEFAULT  3    
     4: 0x0000000000400298   0      SECTION  LOCAL    DEFAULT  4    
     5: 0x00000000004002b8   0      SECTION  LOCAL    DEFAULT  5    
     6: 0x0000000000400300   0      SECTION  LOCAL    DEFAULT  6    
     7: 0x0000000000400338   0      SECTION  LOCAL    DEFAULT  7    
     8: 0x0000000000400340   0      SECTION  LOCAL    DEFAULT  8    
     9: 0x0000000000400360   0      SECTION  LOCAL    DEFAULT  9    
    10: 0x0000000000400378   0      SECTION  LOCAL    DEFAULT  10   
    11: 0x0000000000400390   0      SECTION  LOCAL    DEFAULT  11   
    12: 0x00000000004003b0   0      SECTION  LOCAL    DEFAULT  12   
    13: 0x00000000004003d0   0      SECTION  LOCAL    DEFAULT  13   
    14: 0x00000000004003e0   0      SECTION  LOCAL    DEFAULT  14   
    15: 0x0000000000400574   0      SECTION  LOCAL    DEFAULT  15   
    16: 0x0000000000400580   0      SECTION  LOCAL    DEFAULT  16   
    17: 0x0000000000400584   0      SECTION  LOCAL    DEFAULT  17   
    18: 0x00000000004005b8   0      SECTION  LOCAL    DEFAULT  18   
    19: 0x0000000000600e10   0      SECTION  LOCAL    DEFAULT  19   
    20: 0x0000000000600e18   0      SECTION  LOCAL    DEFAULT  20   
    21: 0x0000000000600e20   0      SECTION  LOCAL    DEFAULT  21   
    22: 0x0000000000600e28   0      SECTION  LOCAL    DEFAULT  22   
    23: 0x0000000000600ff8   0      SECTION  LOCAL    DEFAULT  23   
    24: 0x0000000000601000   0      SECTION  LOCAL    DEFAULT  24   
    25: 0x0000000000601020   0      SECTION  LOCAL    DEFAULT  25   
    26: 0x0000000000601076   0      SECTION  LOCAL    DEFAULT  26   
    27: 0x0000000000000000   0      SECTION  LOCAL    DEFAULT  27   
    28: 0x0000000000000000   0      FILE     LOCAL    DEFAULT  ABS  crtstuff.c
    29: 0x0000000000600e20   0      OBJECT   LOCAL    DEFAULT  21   __JCR_LIST__
    30: 0x0000000000400410   0      FUNC     LOCAL    DEFAULT  14   deregister_tm_clones
    31: 0x0000000000400450   0      FUNC     LOCAL    DEFAULT  14   register_tm_clones
    32: 0x0000000000400490   0      FUNC     LOCAL    DEFAULT  14   __do_global_dtors_aux
    33: 0x0000000000601076   1      OBJECT   LOCAL    DEFAULT  26   completed.7594
    34: 0x0000000000600e18   0      OBJECT   LOCAL    DEFAULT  20   __do_global_dtors_aux_fini_array_entry
    35: 0x00000000004004b0   0      FUNC     LOCAL    DEFAULT  14   frame_dummy
    36: 0x0000000000600e10   0      OBJECT   LOCAL    DEFAULT  19   __frame_dummy_init_array_entry
    37: 0x0000000000000000   0      FILE     LOCAL    DEFAULT  ABS  inline.c
    38: 0x0000000000000000   0      FILE     LOCAL    DEFAULT  ABS  crtstuff.c
    39: 0x00000000004006a8   0      OBJECT   LOCAL    DEFAULT  18   __FRAME_END__
    40: 0x0000000000600e20   0      OBJECT   LOCAL    DEFAULT  21   __JCR_END__
    41: 0x0000000000000000   0      FILE     LOCAL    DEFAULT  ABS  
    42: 0x0000000000600e18   0      NOTYPE   LOCAL    DEFAULT  19   __init_array_end
    43: 0x0000000000600e28   0      OBJECT   LOCAL    DEFAULT  22   _DYNAMIC
    44: 0x0000000000600e10   0      NOTYPE   LOCAL    DEFAULT  19   __init_array_start
    45: 0x0000000000400584   0      NOTYPE   LOCAL    DEFAULT  17   __GNU_EH_FRAME_HDR
    46: 0x0000000000601000   0      OBJECT   LOCAL    DEFAULT  24   _GLOBAL_OFFSET_TABLE_
    47: 0x0000000000400570   2      FUNC     GLOBAL   DEFAULT  14   __libc_csu_fini
    48: 0x0000000000000000   0      NOTYPE   WEAK     DEFAULT  UND  _ITM_deregisterTMCloneTable
    49: 0x0000000000601020   0      NOTYPE   WEAK     DEFAULT  25   data_start
    50: 0x0000000000601076   0      NOTYPE   GLOBAL   DEFAULT  25   _edata
    51: 0x0000000000400574   0      FUNC     GLOBAL   DEFAULT  15   _fini
    52: 0x0000000000000000   0      FUNC     GLOBAL   DEFAULT  UND  __libc_start_main@@GLIBC_2.2.5
    53: 0x0000000000601020   0      NOTYPE   GLOBAL   DEFAULT  25   __data_start
    54: 0x0000000000000000   0      NOTYPE   WEAK     DEFAULT  UND  __gmon_start__
    55: 0x0000000000601028   0      OBJECT   GLOBAL   HIDDEN   25   __dso_handle
    56: 0x0000000000400580   4      OBJECT   GLOBAL   DEFAULT  16   _IO_stdin_used
    57: 0x0000000000400500   101    FUNC     GLOBAL   DEFAULT  14   __libc_csu_init
    58: 0x0000000000601078   0      NOTYPE   GLOBAL   DEFAULT  26   _end
    59: 0x00000000004003e0   42     FUNC     GLOBAL   DEFAULT  14   _start
    60: 0x0000000000601040   54     OBJECT   GLOBAL   DEFAULT  25   shellcode
    61: 0x0000000000601076   0      NOTYPE   GLOBAL   DEFAULT  26   __bss_start
    62: 0x00000000004004d6   34     FUNC     GLOBAL   DEFAULT  14   main
    63: 0x0000000000000000   0      NOTYPE   WEAK     DEFAULT  UND  _Jv_RegisterClasses
    64: 0x0000000000601078   0      OBJECT   GLOBAL   HIDDEN   25   __TMC_END__
    65: 0x0000000000000000   0      NOTYPE   WEAK     DEFAULT  UND  _ITM_registerTMCloneTable
    66: 0x0000000000400390   0      FUNC     GLOBAL   DEFAULT  11   _init
```

* [strip .symtab + .strtab]
```
ⵧ➤ readelf -S $HOME/shell
    .
    .
    .
    [23] .got              PROGBITS         0000000000600ff8  00000ff8
        0000000000000008  0000000000000008  WA       0     0     8
    [24] .got.plt          PROGBITS         0000000000601000  00001000
        0000000000000020  0000000000000008  WA       0     0     8
    [25] .data             PROGBITS         0000000000601020  00001020
        0000000000000056  0000000000000000  WA       0     0     32
    [26] .bss              NOBITS           0000000000601076  00001076
        0000000000000002  0000000000000000  WA       0     0     1
    [27] .comment          PROGBITS         0000000000000000  00001076
        0000000000000035  0000000000000001  MS       0     0     1
    [28] .shstrtab         STRTAB           0000000000000000  00001905
        000000000000010c  0000000000000000           0     0     1
    [29] .symtab           SYMTAB           0000000000000000  000010b0
        0000000000000648  0000000000000018          30    47     8
    [30] .strtab           STRTAB           0000000000000000  000016f8
        000000000000020d  0000000000000000           0     0     1

ⵧ➤ sudo ./symstrip -f $HOME/shell -s

ⵧ➤ readelf -S $HOME/shell
    .
    .
    .
    [23] .got              PROGBITS         0000000000600ff8  00000ff8
        0000000000000008  0000000000000008  WA       0     0     8
    [24] .got.plt          PROGBITS         0000000000601000  00001000
        0000000000000020  0000000000000008  WA       0     0     8
    [25] .data             PROGBITS         0000000000601020  00001020
        0000000000000056  0000000000000000  WA       0     0     32
    [26] .bss              NOBITS           0000000000601076  00001076
        0000000000000002  0000000000000000  WA       0     0     1
    [27] .comment          PROGBITS         0000000000000000  00001076
        0000000000000035  0000000000000001  MS       0     0     1
    [28] .shstrtab         STRTAB           0000000000000000  00001905
        000000000000010c  0000000000000000           0     0     1

```