---
title: "x86 Intrinsics List | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology:  
  - "cpp-tools"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "cl.exe compiler, intrinsics"
  - "intrinsics, x86"
ms.assetid: cd50666a-0f46-4ba1-8308-3a4d3fa43be5
caps.latest.revision: 15
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# x86 Intrinsics List
This document lists intrinsics that the Visual C++ compiler supports when x86 is targeted.  
  
 For information about individual intrinsics, see these resources, as appropriate for the processor you're targeting:  
  
-   The header file. Many intrinsics are documented in comments in the header file.  
  
-   [Intel Intrinsics Guide](http://go.microsoft.com/fwlink/p/?LinkId=512130). Use the search box to find specific intrinsics.  
  
-   [Intel 64 and IA-32 Architectures Software Developer Manuals](http://go.microsoft.com/fwlink/p/?LinkId=251198)  
  
-   [Intel Architecture Instruction Set Extensions Programming Reference](http://go.microsoft.com/fwlink/p/?LinkId=506627)  
  
-   [Intel AVX](http://go.microsoft.com/fwlink/p/?LinkId=251202)  
  
-   [AMD Developer Guides & Manuals](http://go.microsoft.com/fwlink/p/?LinkId=251203)  
  
 The following table lists the intrinsics available on x86 processors. The Technology column lists required instruction-set support. Use the [__cpuid](../intrinsics/cpuid-cpuidex.md) intrinsic to determine instruction-set support at run time. If two entries are in one row, they represent different entry points for the same intrinsic. A [1] indicates the intrinsic is available only on AMD processors. A [2] indicates the intrinsic is available only on Intel processors. A [3] indicates the prototype is a macro. The header required for the function prototype is listed in the Header column. The intrin.h header includes both immintrin.h and ammintrin.h for simplicity.  
  
|Intrinsic name|Technology|Header|Function prototype|  
|--------------------|----------------|------------|------------------------|  
|_addcarry_u16||intrin.h|unsigned char _addcarry_u16(unsigned char c_in,unsigned short src1,unsigned short src2,unsigned short *sum)|  
|[_addcarry_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)||intrin.h|unsigned char _addcarry_u32(unsigned char c_in,unsigned int src1,unsigned int src2,unsigned int *sum)|  
|_addcarry_u8||intrin.h|unsigned char _addcarry_u8(unsigned char c_in,unsigned char src1,unsigned char src2,unsigned char *sum)|  
|[_addcarryx_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|ADX [2]|immintrin.h|unsigned char _addcarryx_u32(unsigned char c_in,unsigned int src1,unsigned int src2,unsigned int *sum)|  
|[__addfsbyte](../intrinsics/addfsbyte-addfsword-addfsdword.md)||intrin.h|void __addfsbyte(unsigned long,unsigned char)|  
|[__addfsdword](../intrinsics/addfsbyte-addfsword-addfsdword.md)||intrin.h|void __addfsdword(unsigned long,unsigned long)|  
|[__addfsword](../intrinsics/addfsbyte-addfsword-addfsdword.md)||intrin.h|void __addfsword(unsigned long,unsigned short)|  
|[_AddressOfReturnAddress](../intrinsics/addressofreturnaddress.md)||intrin.h|void * _AddressOfReturnAddress(void)|  
|_andn_u32|BMI [1]|ammintrin.h|unsigned int _andn_u32(unsigned int,unsigned int)|  
|[_bextr_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI|ammintrin.h, immintrin.h|unsigned int _bextr_u32(unsigned int,unsigned int,unsigned int)|  
|_bextri_u32|ABM [1]|ammintrin.h|unsigned int _bextri_u32(unsigned int,unsigned int)|  
|[_BitScanForward](../intrinsics/bitscanforward-bitscanforward64.md)||intrin.h|BOOLEAN _BitScanForward(OUT ULONG* Index,IN ULONG Mask)|  
|[_BitScanReverse](../intrinsics/bitscanreverse-bitscanreverse64.md)||intrin.h|BOOLEAN _BitScanReverse(OUT ULONG* Index,IN ULONG Mask)|  
|[_bittest](../intrinsics/bittest-bittest64.md)||intrin.h|unsigned char _bittest(long const *a,long b)|  
|[_bittestandcomplement](../intrinsics/bittestandcomplement-bittestandcomplement64.md)||intrin.h|unsigned char _bittestandcomplement(long *a,long b)|  
|[_bittestandreset](../intrinsics/bittestandreset-bittestandreset64.md)||intrin.h|unsigned char _bittestandreset(long *a,long b)|  
|[_bittestandset](../intrinsics/bittestandset-bittestandset64.md)||intrin.h|unsigned char _bittestandset(long *a,long b)|  
|_blcfill_u32|ABM [1]|ammintrin.h|unsigned int _blcfill_u32(unsigned int)|  
|_blci_u32|ABM [1]|ammintrin.h|unsigned int _blci_u32(unsigned int)|  
|_blcic_u32|ABM [1]|ammintrin.h|unsigned int _blcic_u32(unsigned int)|  
|_blcmsk_u32|ABM [1]|ammintrin.h|unsigned int _blcmsk_u32(unsigned int)|  
|_blcs_u32|ABM [1]|ammintrin.h|unsigned int _blcs_u32(unsigned int)|  
|_blsfill_u32|ABM [1]|ammintrin.h|unsigned int _blsfill_u32(unsigned int)|  
|[_blsi_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI|ammintrin.h, immintrin.h|unsigned int _blsi_u32(unsigned int)|  
|_blsic_u32|ABM [1]|ammintrin.h|unsigned int _blsic_u32(unsigned int)|  
|[_blsmsk_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI|ammintrin.h, immintrin.h|unsigned int _blsmsk_u32(unsigned int)|  
|[_blsr_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI|ammintrin.h, immintrin.h|unsigned int _blsr_u32(unsigned int)|  
|[_bzhi_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI [2]|immintrin.h|unsigned int _bzhi_u32(unsigned int,unsigned int)|  
|_clac|SMAP|intrin.h|void _clac(void)|  
|[__cpuid](../intrinsics/cpuid-cpuidex.md)||intrin.h|void __cpuid(int *a,int b)|  
|[__cpuidex](../intrinsics/cpuid-cpuidex.md)||intrin.h|void __cpuidex(int *a,int b,int c)|  
|[__debugbreak](../intrinsics/debugbreak.md)||intrin.h|void __debugbreak(void)|  
|[_disable](../intrinsics/disable.md)||intrin.h|void _disable(void)|  
|[__emul](../intrinsics/emul-emulu.md)||intrin.h|__int64 [pascal/cdecl] \__emul(int,int)|  
|[__emulu](../intrinsics/emul-emulu.md)||intrin.h|unsigned __int64 [pascal/cdecl]\__emulu(unsigned int,unsigned int)|  
|[_enable](../intrinsics/enable.md)||intrin.h|void _enable(void)|  
|[__fastfail](../intrinsics/fastfail.md)||intrin.h|void __fastfail(unsigned int)|  
|[_fxrstor](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FXSR [2]|immintrin.h|void _fxrstor(void const*)|  
|[_fxsave](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FXSR [2]|immintrin.h|void _fxsave(void*)|  
|[__getcallerseflags](../intrinsics/getcallerseflags.md)||intrin.h|(unsigned int __getcallerseflags())|  
|[__halt](../intrinsics/halt.md)||intrin.h|void __halt(void)|  
|[__inbyte](../intrinsics/inbyte.md)||intrin.h|unsigned char __inbyte(unsigned short Port)|  
|[__inbytestring](../intrinsics/inbytestring.md)||intrin.h|void __inbytestring(unsigned short Port,unsigned char *Buffer,unsigned long Count)|  
|[__incfsbyte](../intrinsics/incfsbyte-incfsword-incfsdword.md)||intrin.h|void __incfsbyte(unsigned long)|  
|[__incfsdword](../intrinsics/incfsbyte-incfsword-incfsdword.md)||intrin.h|void __incfsdword(unsigned long)|  
|[__incfsword](../intrinsics/incfsbyte-incfsword-incfsdword.md)||intrin.h|void __incfsword(unsigned long)|  
|[__indword](../intrinsics/indword.md)||intrin.h|unsigned long __indword(unsigned short Port)|  
|[__indwordstring](../intrinsics/indwordstring.md)||intrin.h|void __indwordstring(unsigned short Port,unsigned long *Buffer,unsigned long Count)|  
|[__int2c](../intrinsics/int2c.md)||intrin.h|void __int2c(void)|  
|[_InterlockedAddLargeStatistic](../intrinsics/interlockedaddlargestatistic.md)||intrin.h|long _InterlockedAddLargeStatistic(\__int64 volatile *,long)|  
|[_InterlockedAnd](../intrinsics/interlockedand-intrinsic-functions.md)||intrin.h|long _InterlockedAnd(long volatile *,long)|  
|[_InterlockedAnd_HLEAcquire](../intrinsics/interlockedand-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedAnd_HLEAcquire(long volatile *,long)|  
|[_InterlockedAnd_HLERelease](../intrinsics/interlockedand-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedAnd_HLERelease(long volatile *,long)|  
|[_InterlockedAnd16](../intrinsics/interlockedand-intrinsic-functions.md)||intrin.h|short _InterlockedAnd16(short volatile *,short)|  
|[_InterlockedAnd8](../intrinsics/interlockedand-intrinsic-functions.md)||intrin.h|char _InterlockedAnd8(char volatile *,char)|  
|[_interlockedbittestandreset](../intrinsics/interlockedbittestandreset-intrinsic-functions.md)||intrin.h|unsigned char _interlockedbittestandreset(long *a,long b)|  
|[_interlockedbittestandreset_HLEAcquire](../intrinsics/interlockedbittestandreset-intrinsic-functions.md)|HLE [2]|immintrin.h|unsigned char _interlockedbittestandreset_HLEAcquire(long *a,long b)|  
|[_interlockedbittestandreset_HLERelease](../intrinsics/interlockedbittestandreset-intrinsic-functions.md)|HLE [2]|immintrin.h|unsigned char _interlockedbittestandreset_HLERelease(long *a,long b)|  
|[_interlockedbittestandset](../intrinsics/interlockedbittestandset-intrinsic-functions.md)||intrin.h|unsigned char _interlockedbittestandset(long *a,long b)|  
|[_interlockedbittestandset_HLEAcquire](../intrinsics/interlockedbittestandset-intrinsic-functions.md)|HLE [2]|immintrin.h|unsigned char _interlockedbittestandset_HLEAcquire(long *a,long b)|  
|[_interlockedbittestandset_HLERelease](../intrinsics/interlockedbittestandset-intrinsic-functions.md)|HLE [2]|immintrin.h|unsigned char _interlockedbittestandset_HLERelease(long *a,long b)|  
|[_InterlockedCompareExchange](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)||intrin.h|long _InterlockedCompareExchange (long volatile *,long,long)|  
|[_InterlockedCompareExchange_HLEAcquire](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedCompareExchange_HLEAcquire(long volatile *,long,long)|  
|[_InterlockedCompareExchange_HLERelease](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedCompareExchange_HLERelease(long volatile *,long,long)|  
|[_InterlockedCompareExchange16](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)||intrin.h|short _InterlockedCompareExchange16(short volatile *Destination,short Exchange,short Comparand)|  
|[_InterlockedCompareExchange64](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)||intrin.h|__int64 _InterlockedCompareExchange64(\__int64 volatile *,\__int64,\__int64)|  
|[_InterlockedCompareExchange64_HLEAcquire](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)|HLE [2]|immintrin.h|__int64 _InterlockedCompareExchange64_HLEAcquire(\__int64 volatile *,\__int64,\__int64)|  
|[_InterlockedCompareExchange64_HLERelease](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)|HLE [2]|immintrin.h|__int64 _InterlockedCompareExchange64_HLERelease(\__int64 volatile *,\__int64,\__int64)|  
|[_InterlockedCompareExchange8](../intrinsics/interlockedcompareexchange-intrinsic-functions.md)||intrin.h|char _InterlockedCompareExchange8(char volatile *Destination,char Exchange,char Comparand)|  
|[_InterlockedCompareExchangePointer](../intrinsics/interlockedcompareexchangepointer-intrinsic-functions.md)||intrin.h|void *_InterlockedCompareExchangePointer (void \*volatile \*,void \*,void \*)|  
|[_InterlockedCompareExchangePointer_HLEAcquire](../intrinsics/interlockedcompareexchangepointer-intrinsic-functions.md)|HLE [2]|immintrin.h|void *_InterlockedCompareExchangePointer_HLEAcquire(void \*volatile \*,void \*,void \*)|  
|[_InterlockedCompareExchangePointer_HLERelease](../intrinsics/interlockedcompareexchangepointer-intrinsic-functions.md)|HLE [2]|immintrin.h|void *_InterlockedCompareExchangePointer_HLERelease(void \*volatile \*,void \*,void \*)|  
|[_InterlockedDecrement](../intrinsics/interlockeddecrement-intrinsic-functions.md)||intrin.h|long _InterlockedDecrement(long volatile *)|  
|[_InterlockedDecrement16](../intrinsics/interlockeddecrement-intrinsic-functions.md)||intrin.h|short _InterlockedDecrement16(short volatile *Addend)|  
|[_InterlockedExchange](../intrinsics/interlockedexchange-intrinsic-functions.md)||intrin.h|long _InterlockedExchange(long volatile *,long)|  
|[_InterlockedExchange_HLEAcquire](../intrinsics/interlockedexchange-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedExchange_HLEAcquire(long volatile *,long)|  
|[_InterlockedExchange_HLERelease](../intrinsics/interlockedexchange-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedExchange_HLERelease(long volatile *,long)|  
|[_InterlockedExchange16](../intrinsics/interlockedexchange-intrinsic-functions.md)||intrin.h|short _InterlockedExchange16(short volatile *,short)|  
|[_InterlockedExchange8](../intrinsics/interlockedexchange-intrinsic-functions.md)||intrin.h|char _InterlockedExchange8(char volatile *,char)|  
|[_InterlockedExchangeAdd](../intrinsics/interlockedexchangeadd-intrinsic-functions.md)||intrin.h|long _InterlockedExchangeAdd(long volatile *,long)|  
|[_InterlockedExchangeAdd_HLEAcquire](../intrinsics/interlockedexchangeadd-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedExchangeAdd_HLEAcquire(long volatile *,long)|  
|[_InterlockedExchangeAdd_HLERelease](../intrinsics/interlockedexchangeadd-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedExchangeAdd_HLERelease(long volatile *,long)|  
|[_InterlockedExchangeAdd16](../intrinsics/interlockedexchangeadd-intrinsic-functions.md)||intrin.h|short _InterlockedExchangeAdd16(short volatile *,short)|  
|[_InterlockedExchangeAdd8](../intrinsics/interlockedexchangeadd-intrinsic-functions.md)||intrin.h|char _InterlockedExchangeAdd8(char volatile *,char)|  
|[_InterlockedExchangePointer](../intrinsics/interlockedexchangepointer-intrinsic-functions.md)||intrin.h|void * _InterlockedExchangePointer(void \*volatile \*,void \*)|  
|[_InterlockedExchangePointer_HLEAcquire](../intrinsics/interlockedexchangepointer-intrinsic-functions.md)|HLE [2]|immintrin.h|void * _InterlockedExchangePointer_HLEAcquire(void \*volatile \*,void \*)|  
|[_InterlockedExchangePointer_HLERelease](../intrinsics/interlockedexchangepointer-intrinsic-functions.md)|HLE [2]|immintrin.h|void * _InterlockedExchangePointer_HLERelease(void \*volatile \*,void \*)|  
|[_InterlockedIncrement](../intrinsics/interlockedincrement-intrinsic-functions.md)||intrin.h|long _InterlockedIncrement(long volatile *)|  
|[_InterlockedIncrement16](../intrinsics/interlockedincrement-intrinsic-functions.md)||intrin.h|short _InterlockedIncrement16(short volatile *Addend)|  
|[_InterlockedOr](../intrinsics/interlockedor-intrinsic-functions.md)||intrin.h|long _InterlockedOr(long volatile *,long)|  
|[_InterlockedOr_HLEAcquire](../intrinsics/interlockedor-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedOr_HLEAcquire(long volatile *,long)|  
|[_InterlockedOr_HLERelease](../intrinsics/interlockedor-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedOr_HLERelease(long volatile *,long)|  
|[_InterlockedOr16](../intrinsics/interlockedor-intrinsic-functions.md)||intrin.h|short _InterlockedOr16(short volatile *,short)|  
|[_InterlockedOr8](../intrinsics/interlockedor-intrinsic-functions.md)||intrin.h|char _InterlockedOr8(char volatile *,char)|  
|[_InterlockedXor](../intrinsics/interlockedxor-intrinsic-functions.md)||intrin.h|long _InterlockedXor(long volatile *,long)|  
|[_InterlockedXor_HLEAcquire](../intrinsics/interlockedxor-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedXor_HLEAcquire(long volatile *,long)|  
|[_InterlockedXor_HLERelease](../intrinsics/interlockedxor-intrinsic-functions.md)|HLE [2]|immintrin.h|long _InterlockedXor_HLERelease(long volatile *,long)|  
|[_InterlockedXor16](../intrinsics/interlockedxor-intrinsic-functions.md)||intrin.h|short _InterlockedXor16(short volatile *,short)|  
|[_InterlockedXor8](../intrinsics/interlockedxor-intrinsic-functions.md)||intrin.h|char _InterlockedXor8(char volatile *,char)|  
|[__invlpg](../intrinsics/invlpg.md)||intrin.h|void __invlpg(void*)|  
|[_invpcid](http://go.microsoft.com/fwlink/p/?LinkId=512130)|INVPCID [2]|immintrin.h|void _invpcid(unsigned int,void *)|  
|[__inword](../intrinsics/inword.md)||intrin.h|unsigned short __inword(unsigned short Port)|  
|[__inwordstring](../intrinsics/inwordstring.md)||intrin.h|void __inwordstring(unsigned short Port,unsigned short *Buffer,unsigned long Count)|  
|_lgdt||intrin.h|void _lgdt(void*)|  
|[__lidt](../intrinsics/lidt.md)||intrin.h|void __lidt(void*)|  
|[__ll_lshift](../intrinsics/ll-lshift.md)||intrin.h|unsigned __int64 [pascal/cdecl] \__ll_lshift(unsigned \__int64,int)|  
|[__ll_rshift](../intrinsics/ll-rshift.md)||intrin.h|__int64 [pascal/cdecl] \__ll_rshift(\__int64,int)|  
|_load_be_u16<br /><br /> [_loadbe_i16](https://software.intel.com/sites/landingpage/IntrinsicsGuide/#text=_loadbe_i16&expand=3071)|MOVBE|immintrin.h|unsigned short _load_be_u16(void const*);<br /><br /> short _loadbe_i16(void const\*); [3]|  
|_load_be_u32<br /><br /> [_loadbe_i32](https://software.intel.com/sites/landingpage/IntrinsicsGuide/#text=_loadbe_i32&expand=3072)|MOVBE|immintrin.h|unsigned int _load_be_u32(void const*);<br /><br /> int _loadbe_i32(void const\*); [3]|  
|__llwpcb|LWP [1]|ammintrin.h|void __llwpcb(void *)|  
|__lwpins32|LWP [1]|ammintrin.h|unsigned char __lwpins32(unsigned int,unsigned int,unsigned int)|  
|__lwpval32|LWP [1]|ammintrin.h|void __lwpval32(unsigned int,unsigned int,unsigned int)|  
|[__lzcnt](../intrinsics/lzcnt16-lzcnt-lzcnt64.md)|LZCNT|intrin.h|unsigned int __lzcnt(unsigned int)|  
|[_lzcnt_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI|ammintrin.h, immintrin.h|unsigned int _lzcnt_u32(unsigned int)|  
|[__lzcnt16](../intrinsics/lzcnt16-lzcnt-lzcnt64.md)|LZCNT|intrin.h|unsigned short __lzcnt16(unsigned short)|  
|[_m_empty](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|void _m_empty(void)|  
|_m_femms|3DNOW|intrin.h|void _m_femms(void)|  
|_m_from_float|3DNOW|intrin.h|__m64 _m_from_float(float)|  
|[_m_from_int](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_from_int(int)|  
|[_m_maskmovq](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _m_maskmovq(\__m64,\__m64,char*)|  
|[_m_packssdw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_packssdw(\__m64,\__m64)|  
|[_m_packsswb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_packsswb(\__m64,\__m64)|  
|[_m_packuswb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_packuswb(\__m64,\__m64)|  
|[_m_paddb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddb(\__m64,\__m64)|  
|[_m_paddd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddd(\__m64,\__m64)|  
|[_m_paddsb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddsb(\__m64,\__m64)|  
|[_m_paddsw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddsw(\__m64,\__m64)|  
|[_m_paddusb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddusb(\__m64,\__m64)|  
|[_m_paddusw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddusw(\__m64,\__m64)|  
|[_m_paddw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_paddw(\__m64,\__m64)|  
|[_m_pand](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pand(\__m64,\__m64)|  
|[_m_pandn](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pandn(\__m64,\__m64)|  
|[_m_pavgb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pavgb(\__m64,\__m64)|  
|_m_pavgusb|3DNOW|intrin.h|__m64 _m_pavgusb(\__m64,\__m64)|  
|[_m_pavgw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pavgw(\__m64,\__m64)|  
|[_m_pcmpeqb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pcmpeqb(\__m64,\__m64)|  
|[_m_pcmpeqd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pcmpeqd(\__m64,\__m64)|  
|[_m_pcmpeqw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pcmpeqw(\__m64,\__m64)|  
|[_m_pcmpgtb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pcmpgtb(\__m64,\__m64)|  
|[_m_pcmpgtd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pcmpgtd(\__m64,\__m64)|  
|[_m_pcmpgtw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pcmpgtw(\__m64,\__m64)|  
|[_m_pextrw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _m_pextrw(\__m64,int)|  
|_m_pf2id|3DNOW|intrin.h|__m64 _m_pf2id(\__m64)|  
|_m_pf2iw|3DNOWEXT|intrin.h|__m64 _m_pf2iw(\__m64)|  
|_m_pfacc|3DNOW|intrin.h|__m64 _m_pfacc(\__m64,\__m64)|  
|_m_pfadd|3DNOW|intrin.h|__m64 _m_pfadd(\__m64,\__m64)|  
|_m_pfcmpeq|3DNOW|intrin.h|__m64 _m_pfcmpeq(\__m64,\__m64)|  
|_m_pfcmpge|3DNOW|intrin.h|__m64 _m_pfcmpge(\__m64,\__m64)|  
|_m_pfcmpgt|3DNOW|intrin.h|__m64 _m_pfcmpgt(\__m64,\__m64)|  
|_m_pfmax|3DNOW|intrin.h|__m64 _m_pfmax(\__m64,\__m64)|  
|_m_pfmin|3DNOW|intrin.h|__m64 _m_pfmin(\__m64,\__m64)|  
|_m_pfmul|3DNOW|intrin.h|__m64 _m_pfmul(\__m64,\__m64)|  
|_m_pfnacc|3DNOWEXT|intrin.h|__m64 _m_pfnacc(\__m64,\__m64)|  
|_m_pfpnacc|3DNOWEXT|intrin.h|__m64 _m_pfpnacc(\__m64,\__m64)|  
|_m_pfrcp|3DNOW|intrin.h|__m64 _m_pfrcp(\__m64)|  
|_m_pfrcpit1|3DNOW|intrin.h|__m64 _m_pfrcpit1(\__m64,\__m64)|  
|_m_pfrcpit2|3DNOW|intrin.h|__m64 _m_pfrcpit2(\__m64,\__m64)|  
|_m_pfrsqit1|3DNOW|intrin.h|__m64 _m_pfrsqit1(\__m64,\__m64)|  
|_m_pfrsqrt|3DNOW|intrin.h|__m64 _m_pfrsqrt(\__m64)|  
|_m_pfsub|3DNOW|intrin.h|__m64 _m_pfsub(\__m64,\__m64)|  
|_m_pfsubr|3DNOW|intrin.h|__m64 _m_pfsubr(\__m64,\__m64)|  
|_m_pi2fd|3DNOW|intrin.h|__m64 _m_pi2fd(\__m64)|  
|_m_pi2fw|3DNOWEXT|intrin.h|__m64 _m_pi2fw(\__m64)|  
|[_m_pinsrw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pinsrw(\__m64,int,int)|  
|[_m_pmaddwd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pmaddwd(\__m64,\__m64)|  
|[_m_pmaxsw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pmaxsw(\__m64,\__m64)|  
|[_m_pmaxub](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pmaxub(\__m64,\__m64)|  
|[_m_pminsw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pminsw(\__m64,\__m64)|  
|[_m_pminub](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pminub(\__m64,\__m64)|  
|[_m_pmovmskb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _m_pmovmskb(\__m64)|  
|_m_pmulhrw|3DNOW|intrin.h|__m64 _m_pmulhrw(\__m64,\__m64)|  
|[_m_pmulhuw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pmulhuw(\__m64,\__m64)|  
|[_m_pmulhw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pmulhw(\__m64,\__m64)|  
|[_m_pmullw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pmullw(\__m64,\__m64)|  
|[_m_por](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_por(\__m64,\__m64)|  
|_m_prefetch|3DNOW|intrin.h|void _m_prefetch(void*)|  
|_m_prefetchw|3DNOW|intrin.h|void _m_prefetchw(void*)|  
|[_m_psadbw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_psadbw(\__m64,\__m64)|  
|[_m_pshufw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _m_pshufw(\__m64,int)|  
|[_m_pslld](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pslld(\__m64,\__m64)|  
|[_m_pslldi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pslldi(\__m64,int)|  
|[_m_psllq](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psllq(\__m64,\__m64)|  
|[_m_psllqi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psllqi(\__m64,int)|  
|[_m_psllw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psllw(\__m64,\__m64)|  
|[_m_psllwi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psllwi(\__m64,int)|  
|[_m_psrad](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrad(\__m64,\__m64)|  
|[_m_psradi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psradi(\__m64,int)|  
|[_m_psraw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psraw(\__m64,\__m64)|  
|[_m_psrawi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrawi(\__m64,int)|  
|[_m_psrld](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrld(\__m64,\__m64)|  
|[_m_psrldi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrldi(\__m64,int)|  
|[_m_psrlq](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrlq(\__m64,\__m64)|  
|[_m_psrlqi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrlqi(\__m64,int)|  
|[_m_psrlw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrlw(\__m64,\__m64)|  
|[_m_psrlwi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psrlwi(\__m64,int)|  
|[_m_psubb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubb(\__m64,\__m64)|  
|[_m_psubd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubd(\__m64,\__m64)|  
|[_m_psubsb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubsb(\__m64,\__m64)|  
|[_m_psubsw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubsw(\__m64,\__m64)|  
|[_m_psubusb](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubusb(\__m64,\__m64)|  
|[_m_psubusw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubusw(\__m64,\__m64)|  
|[_m_psubw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_psubw(\__m64,\__m64)|  
|_m_pswapd|3DNOWEXT|intrin.h|__m64 _m_pswapd(\__m64)|  
|[_m_punpckhbw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_punpckhbw(\__m64,\__m64)|  
|[_m_punpckhdq](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_punpckhdq(\__m64,\__m64)|  
|[_m_punpckhwd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_punpckhwd(\__m64,\__m64)|  
|[_m_punpcklbw](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_punpcklbw(\__m64,\__m64)|  
|[_m_punpckldq](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_punpckldq(\__m64,\__m64)|  
|[_m_punpcklwd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_punpcklwd(\__m64,\__m64)|  
|[_m_pxor](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _m_pxor(\__m64,\__m64)|  
|_m_to_float|3DNOW|intrin.h|float _m_to_float(\__m64)|  
|[_m_to_int](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|int _m_to_int(\__m64)|  
|[_mm_abs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_abs_epi16(\__m128i)|  
|[_mm_abs_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_abs_epi32(\__m128i)|  
|[_mm_abs_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_abs_epi8(\__m128i)|  
|[_mm_abs_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_abs_pi16(\__m64)|  
|[_mm_abs_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_abs_pi32(\__m64)|  
|[_mm_abs_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_abs_pi8(\__m64)|  
|[_mm_add_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_add_epi16(\__m128i,\__m128i)|  
|[_mm_add_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_add_epi32(\__m128i,\__m128i)|  
|[_mm_add_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_add_epi64(\__m128i,\__m128i)|  
|[_mm_add_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_add_epi8(\__m128i,\__m128i)|  
|[_mm_add_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_add_pd(\__m128d,\__m128d)|  
|[_mm_add_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_add_ps(\__m128,\__m128)|  
|[_mm_add_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_add_sd(\__m128d,\__m128d)|  
|[_mm_add_si64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m64 _mm_add_si64(\__m64,\__m64)|  
|[_mm_add_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_add_ss(\__m128,\__m128)|  
|[_mm_adds_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_adds_epi16(\__m128i,\__m128i)|  
|[_mm_adds_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_adds_epi8(\__m128i,\__m128i)|  
|[_mm_adds_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_adds_epu16(\__m128i,\__m128i)|  
|[_mm_adds_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_adds_epu8(\__m128i,\__m128i)|  
|[_mm_addsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128d _mm_addsub_pd(\__m128d,\__m128d)|  
|[_mm_addsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128 _mm_addsub_ps(\__m128,\__m128)|  
|[_mm_aesdec_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AESNI [2]|immintrin.h|__m128i _mm_aesdec_si128( \__m128i,\__m128i )|  
|[_mm_aesdeclast_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AESNI [2]|immintrin.h|__m128i _mm_aesdeclast_si128( \__m128i,\__m128i )|  
|[_mm_aesenc_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AESNI [2]|immintrin.h|__m128i _mm_aesenc_si128( \__m128i,\__m128i )|  
|[_mm_aesenclast_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AESNI [2]|immintrin.h|__m128i _mm_aesenclast_si128( \__m128i,\__m128i )|  
|[_mm_aesimc_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AESNI [2]|immintrin.h|__m128i _mm_aesimc_si128 (\__m128i )|  
|[_mm_aeskeygenassist_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AESNI [2]|immintrin.h|__m128i _mm_aeskeygenassist_si128 (\__m128i,const int )|  
|[_mm_alignr_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_alignr_epi8(\__m128i,\__m128i,int)|  
|[_mm_alignr_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_alignr_pi8(\__m64,\__m64,int)|  
|[_mm_and_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_and_pd(\__m128d,\__m128d)|  
|[_mm_and_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_and_ps(\__m128,\__m128)|  
|[_mm_and_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_and_si128(\__m128i,\__m128i)|  
|[_mm_andnot_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_andnot_pd(\__m128d,\__m128d)|  
|[_mm_andnot_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_andnot_ps(\__m128,\__m128)|  
|[_mm_andnot_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_andnot_si128(\__m128i,\__m128i)|  
|[_mm_avg_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_avg_epu16(\__m128i,\__m128i)|  
|[_mm_avg_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_avg_epu8(\__m128i,\__m128i)|  
|[_mm_blend_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_blend_epi16 (\__m128i,\__m128i,const int )|  
|[_mm_blend_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_blend_epi32(\__m128i,\__m128i,const int)|  
|[_mm_blend_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128d _mm_blend_pd (\__m128d,\__m128d,const int )|  
|[_mm_blend_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128  _mm_blend_ps (\__m128,\__m128,const int )|  
|[_mm_blendv_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_blendv_epi8 (\__m128i,\__m128i,\__m128i )|  
|[_mm_blendv_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128d _mm_blendv_pd(\__m128d,\__m128d,\__m128d)|  
|[_mm_blendv_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128  _mm_blendv_ps(\__m128,\__m128,\__m128 )|  
|[_mm_broadcast_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm_broadcast_ss(float const *)|  
|[_mm_broadcastb_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_broadcastb_epi8(\__m128i)|  
|[_mm_broadcastd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_broadcastd_epi32(\__m128i)|  
|[_mm_broadcastq_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_broadcastq_epi64(\__m128i)|  
|[_mm_broadcastsd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128d _mm_broadcastsd_pd(\__m128d)|  
|[_mm_broadcastss_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm_broadcastss_ps(\__m128)|  
|[_mm_broadcastw_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_broadcastw_epi16(\__m128i)|  
|[_mm_castpd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128  _mm_castpd_ps(\__m128d)|  
|[_mm_castpd_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_castpd_si128(\__m128d)|  
|[_mm_castps_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128d _mm_castps_pd(\__m128)|  
|[_mm_castps_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_castps_si128(\__m128)|  
|[_mm_castsi128_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128d _mm_castsi128_pd(\__m128i)|  
|[_mm_castsi128_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128  _mm_castsi128_ps(\__m128i)|  
|[_mm_clflush](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_clflush(void const *)|  
|[_mm_clmulepi64_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|PCLMULQDQ [2]|immintrin.h|__m128i _mm_clmulepi64_si128 (\__m128i,\__m128i,const int )|  
|_mm_cmov_si128|XOP [1]|ammintrin.h|__m128i _mm_cmov_si128(\__m128i,\__m128i,\__m128i)|  
|[_mm_cmp_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d  _mm_cmp_pd(\__m128d,\__m128d,const int)|  
|[_mm_cmp_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128  _mm_cmp_ps(\__m128,\__m128,const int)|  
|[_mm_cmp_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d  _mm_cmp_sd(\__m128d,\__m128d,const int)|  
|[_mm_cmp_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128  _mm_cmp_ss(\__m128,\__m128,const int)|  
|[_mm_cmpeq_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmpeq_epi16(\__m128i,\__m128i)|  
|[_mm_cmpeq_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmpeq_epi32(\__m128i,\__m128i)|  
|[_mm_cmpeq_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cmpeq_epi64(\__m128i,\__m128i )|  
|[_mm_cmpeq_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmpeq_epi8(\__m128i,\__m128i)|  
|[_mm_cmpeq_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpeq_pd(\__m128d,\__m128d)|  
|[_mm_cmpeq_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpeq_ps(\__m128,\__m128)|  
|[_mm_cmpeq_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpeq_sd(\__m128d,\__m128d)|  
|[_mm_cmpeq_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpeq_ss(\__m128,\__m128)|  
|[_mm_cmpestra](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpestra(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpestrc](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpestrc(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpestri](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpestri(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpestrm](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|__m128i _mm_cmpestrm(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpestro](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpestro(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpestrs](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpestrs(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpestrz](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpestrz(\__m128i,int,\__m128i,int,const int)|  
|[_mm_cmpge_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpge_pd(\__m128d,\__m128d)|  
|[_mm_cmpge_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpge_ps(\__m128,\__m128)|  
|[_mm_cmpge_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpge_sd(\__m128d,\__m128d)|  
|[_mm_cmpge_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpge_ss(\__m128,\__m128)|  
|[_mm_cmpgt_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmpgt_epi16(\__m128i,\__m128i)|  
|[_mm_cmpgt_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmpgt_epi32(\__m128i,\__m128i)|  
|[_mm_cmpgt_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|__m128i _mm_cmpgt_epi64(\__m128i,\__m128i )|  
|[_mm_cmpgt_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmpgt_epi8(\__m128i,\__m128i)|  
|[_mm_cmpgt_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpgt_pd(\__m128d,\__m128d)|  
|[_mm_cmpgt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpgt_ps(\__m128,\__m128)|  
|[_mm_cmpgt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpgt_sd(\__m128d,\__m128d)|  
|[_mm_cmpgt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpgt_ss(\__m128,\__m128)|  
|[_mm_cmpistra](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpistra(\__m128i,\__m128i,const int)|  
|[_mm_cmpistrc](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpistrc(\__m128i,\__m128i,const int)|  
|[_mm_cmpistri](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpistri(\__m128i,\__m128i,const int)|  
|[_mm_cmpistrm](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|__m128i _mm_cmpistrm(\__m128i,\__m128i,const int)|  
|[_mm_cmpistro](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpistro(\__m128i,\__m128i,const int)|  
|[_mm_cmpistrs](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpistrs(\__m128i,\__m128i,const int)|  
|[_mm_cmpistrz](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|int _mm_cmpistrz(\__m128i,\__m128i,const int)|  
|[_mm_cmple_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmple_pd(\__m128d,\__m128d)|  
|[_mm_cmple_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmple_ps(\__m128,\__m128)|  
|[_mm_cmple_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmple_sd(\__m128d,\__m128d)|  
|[_mm_cmple_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmple_ss(\__m128,\__m128)|  
|[_mm_cmplt_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmplt_epi16(\__m128i,\__m128i)|  
|[_mm_cmplt_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmplt_epi32(\__m128i,\__m128i)|  
|[_mm_cmplt_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cmplt_epi8(\__m128i,\__m128i)|  
|[_mm_cmplt_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmplt_pd(\__m128d,\__m128d)|  
|[_mm_cmplt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmplt_ps(\__m128,\__m128)|  
|[_mm_cmplt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmplt_sd(\__m128d,\__m128d)|  
|[_mm_cmplt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmplt_ss(\__m128,\__m128)|  
|[_mm_cmpneq_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpneq_pd(\__m128d,\__m128d)|  
|[_mm_cmpneq_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpneq_ps(\__m128,\__m128)|  
|[_mm_cmpneq_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpneq_sd(\__m128d,\__m128d)|  
|[_mm_cmpneq_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpneq_ss(\__m128,\__m128)|  
|[_mm_cmpnge_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpnge_pd(\__m128d,\__m128d)|  
|[_mm_cmpnge_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpnge_ps(\__m128,\__m128)|  
|[_mm_cmpnge_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpnge_sd(\__m128d,\__m128d)|  
|[_mm_cmpnge_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpnge_ss(\__m128,\__m128)|  
|[_mm_cmpngt_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpngt_pd(\__m128d,\__m128d)|  
|[_mm_cmpngt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpngt_ps(\__m128,\__m128)|  
|[_mm_cmpngt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpngt_sd(\__m128d,\__m128d)|  
|[_mm_cmpngt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpngt_ss(\__m128,\__m128)|  
|[_mm_cmpnle_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpnle_pd(\__m128d,\__m128d)|  
|[_mm_cmpnle_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpnle_ps(\__m128,\__m128)|  
|[_mm_cmpnle_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpnle_sd(\__m128d,\__m128d)|  
|[_mm_cmpnle_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpnle_ss(\__m128,\__m128)|  
|[_mm_cmpnlt_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpnlt_pd(\__m128d,\__m128d)|  
|[_mm_cmpnlt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpnlt_ps(\__m128,\__m128)|  
|[_mm_cmpnlt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpnlt_sd(\__m128d,\__m128d)|  
|[_mm_cmpnlt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpnlt_ss(\__m128,\__m128)|  
|[_mm_cmpord_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpord_pd(\__m128d,\__m128d)|  
|[_mm_cmpord_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpord_ps(\__m128,\__m128)|  
|[_mm_cmpord_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpord_sd(\__m128d,\__m128d)|  
|[_mm_cmpord_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpord_ss(\__m128,\__m128)|  
|[_mm_cmpunord_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpunord_pd(\__m128d,\__m128d)|  
|[_mm_cmpunord_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpunord_ps(\__m128,\__m128)|  
|[_mm_cmpunord_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cmpunord_sd(\__m128d,\__m128d)|  
|[_mm_cmpunord_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cmpunord_ss(\__m128,\__m128)|  
|_mm_com_epi16|XOP [1]|ammintrin.h|__m128i _mm_com_epi16(\__m128i,\__m128i,int)|  
|_mm_com_epi32|XOP [1]|ammintrin.h|__m128i _mm_com_epi32(\__m128i,\__m128i,int)|  
|_mm_com_epi64|XOP [1]|ammintrin.h|__m128i _mm_com_epi32(\__m128i,\__m128i,int)|  
|_mm_com_epi8|XOP [1]|ammintrin.h|__m128i _mm_com_epi8(\__m128i,\__m128i,int)|  
|_mm_com_epu16|XOP [1]|ammintrin.h|__m128i _mm_com_epu16(\__m128i,\__m128i,int)|  
|_mm_com_epu32|XOP [1]|ammintrin.h|__m128i _mm_com_epu32(\__m128i,\__m128i,int)|  
|_mm_com_epu64|XOP [1]|ammintrin.h|__m128i _mm_com_epu32(\__m128i,\__m128i,int)|  
|_mm_com_epu8|XOP [1]|ammintrin.h|__m128i _mm_com_epu8(\__m128i,\__m128i,int)|  
|[_mm_comieq_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_comieq_sd(\__m128d,\__m128d)|  
|[_mm_comieq_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_comieq_ss(\__m128,\__m128)|  
|[_mm_comige_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_comige_sd(\__m128d,\__m128d)|  
|[_mm_comige_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_comige_ss(\__m128,\__m128)|  
|[_mm_comigt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_comigt_sd(\__m128d,\__m128d)|  
|[_mm_comigt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_comigt_ss(\__m128,\__m128)|  
|[_mm_comile_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_comile_sd(\__m128d,\__m128d)|  
|[_mm_comile_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_comile_ss(\__m128,\__m128)|  
|[_mm_comilt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_comilt_sd(\__m128d,\__m128d)|  
|[_mm_comilt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_comilt_ss(\__m128,\__m128)|  
|[_mm_comineq_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_comineq_sd(\__m128d,\__m128d)|  
|[_mm_comineq_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_comineq_ss(\__m128,\__m128)|  
|[_mm_crc32_u16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|unsigned int _mm_crc32_u16(unsigned int,unsigned short)|  
|[_mm_crc32_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|unsigned int _mm_crc32_u32(unsigned int,unsigned int)|  
|[_mm_crc32_u8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE42|intrin.h|unsigned int _mm_crc32_u8(unsigned int,unsigned char)|  
|[_mm_cvt_pi2ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cvt_pi2ps(\__m128,\__m64)|  
|[_mm_cvt_ps2pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _mm_cvt_ps2pi(\__m128)|  
|[_mm_cvt_si2ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_cvt_si2ss(\__m128,int)|  
|[_mm_cvt_ss2si](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_cvt_ss2si(\__m128)|  
|[_mm_cvtepi16_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepi16_epi32(\__m128i )|  
|[_mm_cvtepi16_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepi16_epi64(\__m128i )|  
|[_mm_cvtepi32_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepi32_epi64(\__m128i )|  
|[_mm_cvtepi32_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cvtepi32_pd(\__m128i)|  
|[_mm_cvtepi32_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128 _mm_cvtepi32_ps(\__m128i)|  
|[_mm_cvtepi8_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepi8_epi16 (\__m128i )|  
|[_mm_cvtepi8_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepi8_epi32 (\__m128i )|  
|[_mm_cvtepi8_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepi8_epi64 (\__m128i )|  
|[_mm_cvtepu16_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepu16_epi32(\__m128i )|  
|[_mm_cvtepu16_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepu16_epi64(\__m128i )|  
|[_mm_cvtepu32_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepu32_epi64(\__m128i )|  
|[_mm_cvtepu8_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepu8_epi16 (\__m128i )|  
|[_mm_cvtepu8_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepu8_epi32 (\__m128i )|  
|[_mm_cvtepu8_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_cvtepu8_epi64 (\__m128i )|  
|[_mm_cvtpd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cvtpd_epi32(\__m128d)|  
|[_mm_cvtpd_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m64 _mm_cvtpd_pi32(\__m128d)|  
|[_mm_cvtpd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128 _mm_cvtpd_ps(\__m128d)|  
|[_mm_cvtph_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|F16C [2]|immintrin.h|__m128 _mm_cvtph_ps(\__m128i)|  
|[_mm_cvtpi32_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cvtpi32_pd(\__m64)|  
|[_mm_cvtps_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cvtps_epi32(\__m128)|  
|[_mm_cvtps_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cvtps_pd(\__m128)|  
|[_mm_cvtps_ph](http://go.microsoft.com/fwlink/p/?LinkId=512130)|F16C [2]|immintrin.h|__m128i _mm_cvtps_ph(\__m128,const int)|  
|[_mm_cvtsd_f64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|double _mm_cvtsd_f64(\__m128d)|  
|[_mm_cvtsd_si32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_cvtsd_si32(\__m128d)|  
|[_mm_cvtsd_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128 _mm_cvtsd_ss(\__m128,\__m128d)|  
|[_mm_cvtsi128_si32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_cvtsi128_si32(\__m128i)|  
|[_mm_cvtsi32_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cvtsi32_sd(\__m128d,int)|  
|[_mm_cvtsi32_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cvtsi32_si128(int)|  
|[_mm_cvtss_f32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|float _mm_cvtss_f32(\__m128)|  
|[_mm_cvtss_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_cvtss_sd(\__m128d,\__m128)|  
|[_mm_cvtt_ps2pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m64 _mm_cvtt_ps2pi(\__m128)|  
|[_mm_cvtt_ss2si](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_cvtt_ss2si(\__m128)|  
|[_mm_cvttpd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cvttpd_epi32(\__m128d)|  
|[_mm_cvttpd_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m64 _mm_cvttpd_pi32(\__m128d)|  
|[_mm_cvttps_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_cvttps_epi32(\__m128)|  
|[_mm_cvttsd_si32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_cvttsd_si32(\__m128d)|  
|[_mm_div_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_div_pd(\__m128d,\__m128d)|  
|[_mm_div_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_div_ps(\__m128,\__m128)|  
|[_mm_div_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_div_sd(\__m128d,\__m128d)|  
|[_mm_div_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_div_ss(\__m128,\__m128)|  
|[_mm_dp_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128d _mm_dp_pd(\__m128d,\__m128d,const int )|  
|[_mm_dp_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128  _mm_dp_ps(\__m128,\__m128,const int )|  
|[_mm_extract_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_extract_epi16(\__m128i,int)|  
|[_mm_extract_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|int   _mm_extract_epi32(\__m128i,const int )|  
|[_mm_extract_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|int   _mm_extract_epi8 (\__m128i,const int )|  
|[_mm_extract_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|int _mm_extract_ps(\__m128,const int )|  
|[_mm_extract_si64](../intrinsics/mm-extract-si64-mm-extracti-si64.md)|SSE4a|intrin.h|__m128i _mm_extract_si64(\__m128i,\__m128i)|  
|[_mm_extracti_si64](../intrinsics/mm-extract-si64-mm-extracti-si64.md)|SSE4a|intrin.h|__m128i _mm_extracti_si64(\__m128i,int,int)|  
|[_mm_fmadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fmadd_pd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fmadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fmadd_ps (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fmadd_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fmadd_sd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fmadd_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fmadd_ss (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fmaddsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fmaddsub_pd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fmaddsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fmaddsub_ps (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fmsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fmsub_pd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fmsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fmsub_ps (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fmsub_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fmsub_sd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fmsub_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fmsub_ss (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fmsubadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fmsubadd_pd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fmsubadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fmsubadd_ps (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fnmadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fnmadd_pd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fnmadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fnmadd_ps (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fnmadd_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fnmadd_sd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fnmadd_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fnmadd_ss (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fnmsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fnmsub_pd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fnmsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fnmsub_ps (\__m128 a,\__m128 b,\__m128 c)|  
|[_mm_fnmsub_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128d _mm_fnmsub_sd (\__m128d a,\__m128d b,\__m128d c)|  
|[_mm_fnmsub_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m128 _mm_fnmsub_ss (\__m128 a,\__m128 b,\__m128 c)|  
|_mm_frcz_pd|XOP [1]|ammintrin.h|__m128d _mm_frcz_pd(\__m128d)|  
|_mm_frcz_ps|XOP [1]|ammintrin.h|__m128 _mm_frcz_ps(\__m128)|  
|_mm_frcz_sd|XOP [1]|ammintrin.h|__m128d _mm_frcz_sd(\__m128d,\__m128d)|  
|_mm_frcz_ss|XOP [1]|ammintrin.h|__m128 _mm_frcz_ss(\__m128,\__m128)|  
|[_mm_getcsr](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|unsigned int _mm_getcsr(void)|  
|[_mm_hadd_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_hadd_epi16(\__m128i,\__m128i)|  
|[_mm_hadd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_hadd_epi32(\__m128i,\__m128i)|  
|[_mm_hadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128d _mm_hadd_pd(\__m128d,\__m128d)|  
|[_mm_hadd_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_hadd_pi16(\__m64,\__m64)|  
|[_mm_hadd_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_hadd_pi32(\__m64,\__m64)|  
|[_mm_hadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128 _mm_hadd_ps(\__m128,\__m128)|  
|_mm_haddd_epi16|XOP [1]|ammintrin.h|__m128i _mm_haddd_epi16(\__m128i)|  
|_mm_haddd_epi8|XOP [1]|ammintrin.h|__m128i _mm_haddd_epi8(\__m128i)|  
|_mm_haddd_epu16|XOP [1]|ammintrin.h|__m128i _mm_haddd_epu16(\__m128i)|  
|_mm_haddd_epu8|XOP [1]|ammintrin.h|__m128i _mm_haddd_epu8(\__m128i)|  
|_mm_haddq_epi16|XOP [1]|ammintrin.h|__m128i _mm_haddq_epi16(\__m128i)|  
|_mm_haddq_epi32|XOP [1]|ammintrin.h|__m128i _mm_haddq_epi32(\__m128i)|  
|_mm_haddq_epi8|XOP [1]|ammintrin.h|__m128i _mm_haddq_epi8(\__m128i)|  
|_mm_haddq_epu16|XOP [1]|ammintrin.h|__m128i _mm_haddq_epu16(\__m128i)|  
|_mm_haddq_epu32|XOP [1]|ammintrin.h|__m128i _mm_haddq_epu32(\__m128i)|  
|_mm_haddq_epu8|XOP [1]|ammintrin.h|__m128i _mm_haddq_epu8(\__m128i)|  
|[_mm_hadds_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_hadds_epi16(\__m128i,\__m128i)|  
|[_mm_hadds_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_hadds_pi16(\__m64,\__m64)|  
|_mm_haddw_epi8|XOP [1]|ammintrin.h|__m128i _mm_haddw_epi8(\__m128i)|  
|_mm_haddw_epu8|XOP [1]|ammintrin.h|__m128i _mm_haddw_epu8(\__m128i)|  
|[_mm_hsub_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_hsub_epi16(\__m128i,\__m128i)|  
|[_mm_hsub_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_hsub_epi32(\__m128i,\__m128i)|  
|[_mm_hsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128d _mm_hsub_pd(\__m128d,\__m128d)|  
|[_mm_hsub_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_hsub_pi16(\__m64,\__m64)|  
|[_mm_hsub_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_hsub_pi32(\__m64,\__m64)|  
|[_mm_hsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128 _mm_hsub_ps(\__m128,\__m128)|  
|_mm_hsubd_epi16|XOP [1]|ammintrin.h|__m128i _mm_hsubd_epi16(\__m128i)|  
|_mm_hsubq_epi32|XOP [1]|ammintrin.h|__m128i _mm_hsubq_epi32(\__m128i)|  
|[_mm_hsubs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_hsubs_epi16(\__m128i,\__m128i)|  
|[_mm_hsubs_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_hsubs_pi16(\__m64,\__m64)|  
|_mm_hsubw_epi8|XOP [1]|ammintrin.h|__m128i _mm_hsubw_epi8(\__m128i)|  
|[_mm_i32gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_i32gather_epi32(int const *base,\__m128i index,const int scale)|  
|[_mm_i32gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_i32gather_epi64(\__int64 const *base,\__m128i index,const int scale)|  
|[_mm_i32gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128d _mm_i32gather_pd(double const *base,\__m128i index,const int scale)|  
|[_mm_i32gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm_i32gather_ps(float const *base,\__m128i index,const int scale)|  
|[_mm_i64gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_i64gather_epi32(int const *base,\__m128i index,const int scale)|  
|[_mm_i64gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_i64gather_epi64(\__int64 const *base,\__m128i index,const int scale)|  
|[_mm_i64gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128d _mm_i64gather_pd(double const *base,\__m128i index,const int scale)|  
|[_mm_i64gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm_i64gather_ps(float const *base,\__m128i index,const int scale)|  
|[_mm_insert_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_insert_epi16(\__m128i,int,int)|  
|[_mm_insert_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_insert_epi32(\__m128i,int,const int )|  
|[_mm_insert_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_insert_epi8 (\__m128i,int,const int )|  
|[_mm_insert_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128 _mm_insert_ps(\__m128,\__m128,const int )|  
|[_mm_insert_si64](../intrinsics/mm-insert-si64-mm-inserti-si64.md)|SSE4a|intrin.h|__m128i _mm_insert_si64(\__m128i,\__m128i)|  
|[_mm_inserti_si64](../intrinsics/mm-insert-si64-mm-inserti-si64.md)|SSE4a|intrin.h|__m128i _mm_inserti_si64(\__m128i,\__m128i,int,int)|  
|[_mm_lddqu_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128i _mm_lddqu_si128(\__m128i const*)|  
|[_mm_lfence](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_lfence(void)|  
|[_mm_load_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_load_pd(double*)|  
|[_mm_load_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_load_ps(float*)|  
|[_mm_load_ps1](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_load_ps1(float*)|  
|[_mm_load_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_load_sd(double*)|  
|[_mm_load_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_load_si128(\__m128i*)|  
|[_mm_load_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_load_ss(float*)|  
|[_mm_load1_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_load1_pd(double*)|  
|[_mm_loaddup_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128d _mm_loaddup_pd(double const*)|  
|[_mm_loadh_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_loadh_pd(\__m128d,double*)|  
|[_mm_loadh_pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_loadh_pi(\__m128,\__m64*)|  
|[_mm_loadl_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_loadl_epi64(\__m128i*)|  
|[_mm_loadl_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_loadl_pd(\__m128d,double*)|  
|[_mm_loadl_pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_loadl_pi(\__m128,\__m64*)|  
|[_mm_loadr_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_loadr_pd(double*)|  
|[_mm_loadr_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_loadr_ps(float*)|  
|[_mm_loadu_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_loadu_pd(double*)|  
|[_mm_loadu_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_loadu_ps(float*)|  
|[_mm_loadu_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_loadu_si128(\__m128i*)|  
|_mm_macc_epi16|XOP [1]|ammintrin.h|__m128i _mm_macc_epi16(\__m128i,\__m128i,\__m128i)|  
|_mm_macc_epi32|XOP [1]|ammintrin.h|__m128i _mm_macc_epi32(\__m128i,\__m128i,\__m128i)|  
|_mm_macc_pd|FMA4 [1]|ammintrin.h|__m128d _mm_macc_pd(\__m128d,\__m128d,\__m128d)|  
|_mm_macc_ps|FMA4 [1]|ammintrin.h|__m128 _mm_macc_ps(\__m128,\__m128,\__m128)|  
|_mm_macc_sd|FMA4 [1]|ammintrin.h|__m128d _mm_macc_sd(\__m128d,\__m128d,\__m128d)|  
|_mm_macc_ss|FMA4 [1]|ammintrin.h|__m128 _mm_macc_ss(\__m128,\__m128,\__m128)|  
|_mm_maccd_epi16|XOP [1]|ammintrin.h|__m128i _mm_maccd_epi16(\__m128i,\__m128i,\__m128i)|  
|_mm_macchi_epi32|XOP [1]|ammintrin.h|__m128i _mm_macchi_epi32(\__m128i,\__m128i,\__m128i)|  
|_mm_macclo_epi32|XOP [1]|ammintrin.h|__m128i _mm_macclo_epi32(\__m128i,\__m128i,\__m128i)|  
|_mm_maccs_epi16|XOP [1]|ammintrin.h|__m128i _mm_maccs_epi16(\__m128i,\__m128i,\__m128i)|  
|_mm_maccs_epi32|XOP [1]|ammintrin.h|__m128i _mm_maccs_epi32(\__m128i,\__m128i,\__m128i)|  
|_mm_maccsd_epi16|XOP [1]|ammintrin.h|__m128i _mm_maccsd_epi16(\__m128i,\__m128i,\__m128i)|  
|_mm_maccshi_epi32|XOP [1]|ammintrin.h|__m128i _mm_maccshi_epi32(\__m128i,\__m128i,\__m128i)|  
|_mm_maccslo_epi32|XOP [1]|ammintrin.h|__m128i _mm_maccslo_epi32(\__m128i,\__m128i,\__m128i)|  
|[_mm_madd_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_madd_epi16(\__m128i,\__m128i)|  
|_mm_maddd_epi16|XOP [1]|ammintrin.h|__m128i _mm_maddd_epi16(\__m128i,\__m128i,\__m128i)|  
|_mm_maddsd_epi16|XOP [1]|ammintrin.h|__m128i _mm_maddsd_epi16(\__m128i,\__m128i,\__m128i)|  
|_mm_maddsub_pd|FMA4 [1]|ammintrin.h|__m128d _mm_maddsub_pd(\__m128d,\__m128d,\__m128d)|  
|_mm_maddsub_ps|FMA4 [1]|ammintrin.h|__m128 _mm_maddsub_ps(\__m128,\__m128,\__m128)|  
|[_mm_maddubs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_maddubs_epi16(\__m128i,\__m128i)|  
|[_mm_maddubs_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_maddubs_pi16(\__m64,\__m64)|  
|[_mm_mask_i32gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_mask_i32gather_epi32(\__m128i src,int const *base,\__m128i index,\__m128i mask,const int scale)|  
|[_mm_mask_i32gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_mask_i32gather_epi64(\__m128i src,\__int64 const *base,\__m128i index,\__m128i mask,const int scale)|  
|[_mm_mask_i32gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128d _mm_mask_i32gather_pd(\__m128d src,double const *base,\__m128i index,\__m128d mask,const int scale)|  
|[_mm_mask_i32gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm_mask_i32gather_ps(\__m128 src,float const *base,\__m128i index,\__m128 mask,const int scale)|  
|[_mm_mask_i64gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_mask_i64gather_epi32(\__m128i src,int const *base,\__m128i index,\__m128i mask,const int scale)|  
|[_mm_mask_i64gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_mask_i64gather_epi64(\__m128i src,\__int64 const *base,\__m128i index,\__m128i mask,const int scale)|  
|[_mm_mask_i64gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128d _mm_mask_i64gather_pd(\__m128d src,double const *base,\__m128i index,\__m128d mask,const int scale)|  
|[_mm_mask_i64gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm_mask_i64gather_ps(\__m128 src,float const *base,\__m128i index,\__m128 mask,const int scale)|  
|[_mm_maskload_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_maskload_epi32(int const *,\__m128i)|  
|[_mm_maskload_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_maskload_epi64( \__int64 const *,\__m128i)|  
|[_mm_maskload_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d _mm_maskload_pd(double const *,\__m128i)|  
|[_mm_maskload_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm_maskload_ps(float const *,\__m128i)|  
|[_mm_maskmoveu_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_maskmoveu_si128(\__m128i,\__m128i,char*)|  
|[_mm_maskstore_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|void _mm_maskstore_epi32(int *,\__m128i,\__m128i)|  
|[_mm_maskstore_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|void _mm_maskstore_epi64(\__int64 *,\__m128i,\__m128i)|  
|[_mm_maskstore_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm_maskstore_pd(double *,\__m128i,\__m128d)|  
|[_mm_maskstore_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm_maskstore_ps(float *,\__m128i,\__m128)|  
|[_mm_max_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_max_epi16(\__m128i,\__m128i)|  
|[_mm_max_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_max_epi32(\__m128i,\__m128i )|  
|[_mm_max_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_max_epi8 (\__m128i,\__m128i )|  
|[_mm_max_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_max_epu16(\__m128i,\__m128i )|  
|[_mm_max_epu32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_max_epu32(\__m128i,\__m128i )|  
|[_mm_max_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_max_epu8(\__m128i,\__m128i)|  
|[_mm_max_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_max_pd(\__m128d,\__m128d)|  
|[_mm_max_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_max_ps(\__m128,\__m128)|  
|[_mm_max_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_max_sd(\__m128d,\__m128d)|  
|[_mm_max_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_max_ss(\__m128,\__m128)|  
|[_mm_mfence](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_mfence(void)|  
|[_mm_min_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_min_epi16(\__m128i,\__m128i)|  
|[_mm_min_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_min_epi32(\__m128i,\__m128i )|  
|[_mm_min_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_min_epi8 (\__m128i,\__m128i )|  
|[_mm_min_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_min_epu16(\__m128i,\__m128i )|  
|[_mm_min_epu32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_min_epu32(\__m128i,\__m128i )|  
|[_mm_min_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_min_epu8(\__m128i,\__m128i)|  
|[_mm_min_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_min_pd(\__m128d,\__m128d)|  
|[_mm_min_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_min_ps(\__m128,\__m128)|  
|[_mm_min_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_min_sd(\__m128d,\__m128d)|  
|[_mm_min_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_min_ss(\__m128,\__m128)|  
|[_mm_minpos_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_minpos_epu16(\__m128i )|  
|[_mm_monitor](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|void _mm_monitor(void const*,unsigned int,unsigned int)|  
|[_mm_move_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_move_epi64(\__m128i)|  
|[_mm_move_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_move_sd(\__m128d,\__m128d)|  
|[_mm_move_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_move_ss(\__m128,\__m128)|  
|[_mm_movedup_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128d _mm_movedup_pd(\__m128d)|  
|[_mm_movehdup_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128 _mm_movehdup_ps(\__m128)|  
|[_mm_movehl_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_movehl_ps(\__m128,\__m128)|  
|[_mm_moveldup_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|__m128 _mm_moveldup_ps(\__m128)|  
|[_mm_movelh_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_movelh_ps(\__m128,\__m128)|  
|[_mm_movemask_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_movemask_epi8(\__m128i)|  
|[_mm_movemask_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_movemask_pd(\__m128d)|  
|[_mm_movemask_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_movemask_ps(\__m128)|  
|[_mm_movepi64_pi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m64 _mm_movepi64_pi64(\__m128i)|  
|[_mm_movpi64_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_movpi64_epi64(\__m64)|  
|[_mm_mpsadbw_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_mpsadbw_epu8(\__m128i s1,\__m128i,const int)|  
|_mm_msub_pd|FMA4 [1]|ammintrin.h|__m128d _mm_msub_pd(\__m128d,\__m128d,\__m128d)|  
|_mm_msub_ps|FMA4 [1]|ammintrin.h|__m128 _mm_msub_ps(\__m128,\__m128,\__m128)|  
|_mm_msub_sd|FMA4 [1]|ammintrin.h|__m128d _mm_msub_sd(\__m128d,\__m128d,\__m128d)|  
|_mm_msub_ss|FMA4 [1]|ammintrin.h|__m128 _mm_msub_ss(\__m128,\__m128,\__m128)|  
|_mm_msubadd_pd|FMA4 [1]|ammintrin.h|__m128d _mm_msubadd_pd(\__m128d,\__m128d,\__m128d)|  
|_mm_msubadd_ps|FMA4 [1]|ammintrin.h|__m128 _mm_msubadd_ps(\__m128,\__m128,\__m128)|  
|[_mm_mul_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_mul_epi32(\__m128i,\__m128i )|  
|[_mm_mul_epu32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_mul_epu32(\__m128i,\__m128i)|  
|[_mm_mul_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_mul_pd(\__m128d,\__m128d)|  
|[_mm_mul_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_mul_ps(\__m128,\__m128)|  
|[_mm_mul_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_mul_sd(\__m128d,\__m128d)|  
|[_mm_mul_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_mul_ss(\__m128,\__m128)|  
|[_mm_mul_su32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m64 _mm_mul_su32(\__m64,\__m64)|  
|[_mm_mulhi_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_mulhi_epi16(\__m128i,\__m128i)|  
|[_mm_mulhi_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_mulhi_epu16(\__m128i,\__m128i)|  
|[_mm_mulhrs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_mulhrs_epi16(\__m128i,\__m128i)|  
|[_mm_mulhrs_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_mulhrs_pi16(\__m64,\__m64)|  
|[_mm_mullo_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_mullo_epi16(\__m128i,\__m128i)|  
|[_mm_mullo_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_mullo_epi32(\__m128i,\__m128i )|  
|[_mm_mwait](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE3|intrin.h|void _mm_mwait(unsigned int,unsigned int)|  
|_mm_nmacc_pd|FMA4 [1]|ammintrin.h|__m128d _mm_nmacc_pd(\__m128d,\__m128d,\__m128d)|  
|_mm_nmacc_ps|FMA4 [1]|ammintrin.h|__m128 _mm_nmacc_ps(\__m128,\__m128,\__m128)|  
|_mm_nmacc_sd|FMA4 [1]|ammintrin.h|__m128d _mm_nmacc_sd(\__m128d,\__m128d,\__m128d)|  
|_mm_nmacc_ss|FMA4 [1]|ammintrin.h|__m128 _mm_nmacc_ss(\__m128,\__m128,\__m128)|  
|_mm_nmsub_pd|FMA4 [1]|ammintrin.h|__m128d _mm_nmsub_pd(\__m128d,\__m128d,\__m128d)|  
|_mm_nmsub_ps|FMA4 [1]|ammintrin.h|__m128 _mm_nmsub_ps(\__m128,\__m128,\__m128)|  
|_mm_nmsub_sd|FMA4 [1]|ammintrin.h|__m128d _mm_nmsub_sd(\__m128d,\__m128d,\__m128d)|  
|_mm_nmsub_ss|FMA4 [1]|ammintrin.h|__m128 _mm_nmsub_ss(\__m128,\__m128,\__m128)|  
|[_mm_or_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_or_pd(\__m128d,\__m128d)|  
|[_mm_or_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_or_ps(\__m128,\__m128)|  
|[_mm_or_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_or_si128(\__m128i,\__m128i)|  
|[_mm_packs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_packs_epi16(\__m128i,\__m128i)|  
|[_mm_packs_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_packs_epi32(\__m128i,\__m128i)|  
|[_mm_packus_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_packus_epi16(\__m128i,\__m128i)|  
|[_mm_packus_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_packus_epi32(\__m128i,\__m128i )|  
|[_mm_pause](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_pause(void)|  
|_mm_perm_epi8|XOP [1]|ammintrin.h|__m128i _mm_perm_epi8(\__m128i,\__m128i,\__m128i)|  
|[_mm_permute_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d _mm_permute_pd(\__m128d,int)|  
|[_mm_permute_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm_permute_ps(\__m128,int)|  
|_mm_permute2_pd|XOP [1]|ammintrin.h|__m128d _mm_permute2_pd(\__m128d,\__m128d,\__m128i,int)|  
|_mm_permute2_ps|XOP [1]|ammintrin.h|__m128 _mm_permute2_ps(\__m128,\__m128,\__m128i,int)|  
|[_mm_permutevar_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d _mm_permutevar_pd(\__m128d,\__m128i)|  
|[_mm_permutevar_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm_permutevar_ps(\__m128,\__m128i)|  
|[_mm_popcnt_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|POPCNT|intrin.h|int _mm_popcnt_u32(unsigned int)|  
|[_mm_prefetch](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_prefetch(char*,int)|  
|[_mm_rcp_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_rcp_ps(\__m128)|  
|[_mm_rcp_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_rcp_ss(\__m128)|  
|_mm_rot_epi16|XOP [1]|ammintrin.h|__m128i _mm_rot_epi16(\__m128i,\__m128i)|  
|_mm_rot_epi32|XOP [1]|ammintrin.h|__m128i _mm_rot_epi32(\__m128i,\__m128i)|  
|_mm_rot_epi64|XOP [1]|ammintrin.h|__m128i _mm_rot_epi64(\__m128i,\__m128i)|  
|_mm_rot_epi8|XOP [1]|ammintrin.h|__m128i _mm_rot_epi8(\__m128i,\__m128i)|  
|_mm_roti_epi16|XOP [1]|ammintrin.h|__m128i _mm_rot_epi16(\__m128i,int)|  
|_mm_roti_epi32|XOP [1]|ammintrin.h|__m128i _mm_rot_epi32(\__m128i,int)|  
|_mm_roti_epi64|XOP [1]|ammintrin.h|__m128i _mm_rot_epi64(\__m128i,int)|  
|_mm_roti_epi8|XOP [1]|ammintrin.h|__m128i _mm_rot_epi8(\__m128i,int)|  
|[_mm_round_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128d _mm_round_pd(\__m128d,const int )|  
|[_mm_round_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128  _mm_round_ps(\__m128,const int )|  
|[_mm_round_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128d _mm_round_sd(\__m128d,\__m128d,const int )|  
|[_mm_round_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128  _mm_round_ss(\__m128,\__m128,const int )|  
|[_mm_rsqrt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_rsqrt_ps(\__m128)|  
|[_mm_rsqrt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_rsqrt_ss(\__m128)|  
|[_mm_sad_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sad_epu8(\__m128i,\__m128i)|  
|[_mm_set_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set_epi16(short,short,short,short,short,short,short,short)|  
|[_mm_set_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set_epi32(int,int,int,int)|  
|[_mm_set_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set_epi64(\__m64,\__m64)|  
|[_mm_set_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set_epi8(char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char)|  
|[_mm_set_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_set_pd(double,double)|  
|[_mm_set_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_set_pi16(short,short,short,short)|  
|[_mm_set_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_set_pi32(int,int)|  
|[_mm_set_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_set_pi8(char,char,char,char,char,char,char,char)|  
|[_mm_set_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_set_ps(float,float,float,float)|  
|[_mm_set_ps1](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_set_ps1(float)|  
|[_mm_set_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_set_sd(double)|  
|[_mm_set_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_set_ss(float)|  
|[_mm_set1_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set1_epi16(short)|  
|[_mm_set1_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set1_epi32(int)|  
|[_mm_set1_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set1_epi64(\__m64)|  
|[_mm_set1_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_set1_epi8(char)|  
|[_mm_set1_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_set1_pd(double)|  
|[_mm_set1_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_set1_pi16(short)|  
|[_mm_set1_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_set1_pi32(int)|  
|[_mm_set1_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_set1_pi8(char)|  
|[_mm_setcsr](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_setcsr(unsigned int)|  
|_mm_setl_epi64|SSE2|intrin.h|__m128i _mm_setl_epi64(\__m128i)|  
|[_mm_setr_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_setr_epi16(short,short,short,short,short,short,short,short)|  
|[_mm_setr_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_setr_epi32(int,int,int,int)|  
|[_mm_setr_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_setr_epi64(\__m64,\__m64)|  
|[_mm_setr_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_setr_epi8(char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char)|  
|[_mm_setr_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_setr_pd(double,double)|  
|[_mm_setr_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_setr_pi16(short,short,short,short)|  
|[_mm_setr_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_setr_pi32(int,int)|  
|[_mm_setr_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_setr_pi8(char,char,char,char,char,char,char,char)|  
|[_mm_setr_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_setr_ps(float,float,float,float)|  
|[_mm_setzero_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_setzero_pd(void)|  
|[_mm_setzero_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_setzero_ps(void)|  
|[_mm_setzero_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_setzero_si128(void)|  
|[_mm_setzero_si64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|MMX|intrin.h|__m64 _mm_setzero_si64(void)|  
|[_mm_sfence](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_sfence(void)|  
|_mm_sha_epi16|XOP [1]|ammintrin.h|__m128i _mm_sha_epi16(\__m128i,\__m128i)|  
|_mm_sha_epi32|XOP [1]|ammintrin.h|__m128i _mm_sha_epi32(\__m128i,\__m128i)|  
|_mm_sha_epi64|XOP [1]|ammintrin.h|__m128i _mm_sha_epi64(\__m128i,\__m128i)|  
|_mm_sha_epi8|XOP [1]|ammintrin.h|__m128i _mm_sha_epi8(\__m128i,\__m128i)|  
|_mm_shl_epi16|XOP [1]|ammintrin.h|__m128i _mm_shl_epi16(\__m128i,\__m128i)|  
|_mm_shl_epi32|XOP [1]|ammintrin.h|__m128i _mm_shl_epi32(\__m128i,\__m128i)|  
|_mm_shl_epi64|XOP [1]|ammintrin.h|__m128i _mm_shl_epi64(\__m128i,\__m128i)|  
|_mm_shl_epi8|XOP [1]|ammintrin.h|__m128i _mm_shl_epi8(\__m128i,\__m128i)|  
|[_mm_shuffle_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_shuffle_epi32(\__m128i,int)|  
|[_mm_shuffle_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_shuffle_epi8(\__m128i,\__m128i)|  
|[_mm_shuffle_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_shuffle_pd(\__m128d,\__m128d,int)|  
|[_mm_shuffle_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_shuffle_pi8(\__m64,\__m64)|  
|[_mm_shuffle_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_shuffle_ps(\__m128,\__m128,unsigned int)|  
|[_mm_shufflehi_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_shufflehi_epi16(\__m128i,int)|  
|[_mm_shufflelo_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_shufflelo_epi16(\__m128i,int)|  
|[_mm_sign_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_sign_epi16(\__m128i,\__m128i)|  
|[_mm_sign_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_sign_epi32(\__m128i,\__m128i)|  
|[_mm_sign_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m128i _mm_sign_epi8(\__m128i,\__m128i)|  
|[_mm_sign_pi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_sign_pi16(\__m64,\__m64)|  
|[_mm_sign_pi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_sign_pi32(\__m64,\__m64)|  
|[_mm_sign_pi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSSE3|intrin.h|__m64 _mm_sign_pi8(\__m64,\__m64)|  
|[_mm_sll_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sll_epi16(\__m128i,\__m128i)|  
|[_mm_sll_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sll_epi32(\__m128i,\__m128i)|  
|[_mm_sll_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sll_epi64(\__m128i,\__m128i)|  
|[_mm_slli_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_slli_epi16(\__m128i,int)|  
|[_mm_slli_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_slli_epi32(\__m128i,int)|  
|[_mm_slli_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_slli_epi64(\__m128i,int)|  
|[_mm_slli_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_slli_si128(\__m128i,int)|  
|[_mm_sllv_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_sllv_epi32(\__m128i,\__m128i)|  
|[_mm_sllv_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_sllv_epi64(\__m128i,\__m128i)|  
|[_mm_sqrt_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_sqrt_pd(\__m128d)|  
|[_mm_sqrt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_sqrt_ps(\__m128)|  
|[_mm_sqrt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_sqrt_sd(\__m128d,\__m128d)|  
|[_mm_sqrt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_sqrt_ss(\__m128)|  
|[_mm_sra_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sra_epi16(\__m128i,\__m128i)|  
|[_mm_sra_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sra_epi32(\__m128i,\__m128i)|  
|[_mm_srai_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srai_epi16(\__m128i,int)|  
|[_mm_srai_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srai_epi32(\__m128i,int)|  
|[_mm_srav_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_srav_epi32(\__m128i,\__m128i)|  
|[_mm_srl_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srl_epi16(\__m128i,\__m128i)|  
|[_mm_srl_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srl_epi32(\__m128i,\__m128i)|  
|[_mm_srl_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srl_epi64(\__m128i,\__m128i)|  
|[_mm_srli_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srli_epi16(\__m128i,int)|  
|[_mm_srli_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srli_epi32(\__m128i,int)|  
|[_mm_srli_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srli_epi64(\__m128i,int)|  
|[_mm_srli_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_srli_si128(\__m128i,int)|  
|[_mm_srlv_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_srlv_epi32(\__m128i,\__m128i)|  
|[_mm_srlv_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm_srlv_epi64(\__m128i,\__m128i)|  
|[_mm_store_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_store_pd(double*,\__m128d)|  
|[_mm_store_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_store_ps(float*,\__m128)|  
|[_mm_store_ps1](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_store_ps1(float*,\__m128)|  
|[_mm_store_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_store_sd(double*,\__m128d)|  
|[_mm_store_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_store_si128(\__m128i*,\__m128i)|  
|[_mm_store_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_store_ss(float*,\__m128)|  
|[_mm_store1_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_store1_pd(double*,\__m128d)|  
|[_mm_storeh_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_storeh_pd(double*,\__m128d)|  
|[_mm_storeh_pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_storeh_pi(\__m64*,\__m128)|  
|[_mm_storel_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_storel_epi64(\__m128i*,\__m128i)|  
|[_mm_storel_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_storel_pd(double*,\__m128d)|  
|[_mm_storel_pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_storel_pi(\__m64*,\__m128)|  
|[_mm_storer_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_storer_pd(double*,\__m128d)|  
|[_mm_storer_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_storer_ps(float*,\__m128)|  
|[_mm_storeu_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_storeu_pd(double*,\__m128d)|  
|[_mm_storeu_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_storeu_ps(float*,\__m128)|  
|[_mm_storeu_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_storeu_si128(\__m128i*,\__m128i)|  
|[_mm_stream_load_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|__m128i _mm_stream_load_si128(\__m128i* )|  
|[_mm_stream_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_stream_pd(double*,\__m128d)|  
|[_mm_stream_pi](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_stream_pi(\__m64*,\__m64)|  
|[_mm_stream_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|void _mm_stream_ps(float*,\__m128)|  
|[_mm_stream_sd](../intrinsics/mm-stream-sd.md)|SSE4a|intrin.h|void _mm_stream_sd(double*,\__m128d)|  
|[_mm_stream_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_stream_si128(\__m128i*,\__m128i)|  
|[_mm_stream_si32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|void _mm_stream_si32(int*,int)|  
|[_mm_stream_ss](../intrinsics/mm-stream-ss.md)|SSE4a|intrin.h|void _mm_stream_ss(float*,\__m128)|  
|[_mm_sub_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sub_epi16(\__m128i,\__m128i)|  
|[_mm_sub_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sub_epi32(\__m128i,\__m128i)|  
|[_mm_sub_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sub_epi64(\__m128i,\__m128i)|  
|[_mm_sub_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_sub_epi8(\__m128i,\__m128i)|  
|[_mm_sub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_sub_pd(\__m128d,\__m128d)|  
|[_mm_sub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_sub_ps(\__m128,\__m128)|  
|[_mm_sub_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_sub_sd(\__m128d,\__m128d)|  
|[_mm_sub_si64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m64 _mm_sub_si64(\__m64,\__m64)|  
|[_mm_sub_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_sub_ss(\__m128,\__m128)|  
|[_mm_subs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_subs_epi16(\__m128i,\__m128i)|  
|[_mm_subs_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_subs_epi8(\__m128i,\__m128i)|  
|[_mm_subs_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_subs_epu16(\__m128i,\__m128i)|  
|[_mm_subs_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_subs_epu8(\__m128i,\__m128i)|  
|[_mm_testc_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm_testc_pd(\__m128d,\__m128d)|  
|[_mm_testc_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm_testc_ps(\__m128,\__m128)|  
|[_mm_testc_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|int _mm_testc_si128(\__m128i,\__m128i )|  
|[_mm_testnzc_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm_testnzc_pd(\__m128d,\__m128d)|  
|[_mm_testnzc_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm_testnzc_ps(\__m128,\__m128)|  
|[_mm_testnzc_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|int _mm_testnzc_si128(\__m128i,\__m128i )|  
|[_mm_testz_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm_testz_pd(\__m128d,\__m128d)|  
|[_mm_testz_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm_testz_ps(\__m128,\__m128)|  
|[_mm_testz_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE41|intrin.h|int _mm_testz_si128(\__m128i,\__m128i )|  
|[_mm_ucomieq_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_ucomieq_sd(\__m128d,\__m128d)|  
|[_mm_ucomieq_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_ucomieq_ss(\__m128,\__m128)|  
|[_mm_ucomige_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_ucomige_sd(\__m128d,\__m128d)|  
|[_mm_ucomige_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_ucomige_ss(\__m128,\__m128)|  
|[_mm_ucomigt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_ucomigt_sd(\__m128d,\__m128d)|  
|[_mm_ucomigt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_ucomigt_ss(\__m128,\__m128)|  
|[_mm_ucomile_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_ucomile_sd(\__m128d,\__m128d)|  
|[_mm_ucomile_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_ucomile_ss(\__m128,\__m128)|  
|[_mm_ucomilt_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_ucomilt_sd(\__m128d,\__m128d)|  
|[_mm_ucomilt_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_ucomilt_ss(\__m128,\__m128)|  
|[_mm_ucomineq_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|int _mm_ucomineq_sd(\__m128d,\__m128d)|  
|[_mm_ucomineq_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|int _mm_ucomineq_ss(\__m128,\__m128)|  
|[_mm_unpackhi_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpackhi_epi16(\__m128i,\__m128i)|  
|[_mm_unpackhi_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpackhi_epi32(\__m128i,\__m128i)|  
|[_mm_unpackhi_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpackhi_epi64(\__m128i,\__m128i)|  
|[_mm_unpackhi_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpackhi_epi8(\__m128i,\__m128i)|  
|[_mm_unpackhi_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_unpackhi_pd(\__m128d,\__m128d)|  
|[_mm_unpackhi_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_unpackhi_ps(\__m128,\__m128)|  
|[_mm_unpacklo_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpacklo_epi16(\__m128i,\__m128i)|  
|[_mm_unpacklo_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpacklo_epi32(\__m128i,\__m128i)|  
|[_mm_unpacklo_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpacklo_epi64(\__m128i,\__m128i)|  
|[_mm_unpacklo_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_unpacklo_epi8(\__m128i,\__m128i)|  
|[_mm_unpacklo_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_unpacklo_pd(\__m128d,\__m128d)|  
|[_mm_unpacklo_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_unpacklo_ps(\__m128,\__m128)|  
|[_mm_xor_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128d _mm_xor_pd(\__m128d,\__m128d)|  
|[_mm_xor_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE|intrin.h|__m128 _mm_xor_ps(\__m128,\__m128)|  
|[_mm_xor_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|SSE2|intrin.h|__m128i _mm_xor_si128(\__m128i,\__m128i)|  
|[_mm256_abs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_abs_epi16(\__m256i)|  
|[_mm256_abs_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_abs_epi32(\__m256i)|  
|[_mm256_abs_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_abs_epi8(\__m256i)|  
|[_mm256_add_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_add_epi16(\__m256i,\__m256i)|  
|[_mm256_add_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_add_epi32(\__m256i,\__m256i)|  
|[_mm256_add_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_add_epi64(\__m256i,\__m256i)|  
|[_mm256_add_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_add_epi8(\__m256i,\__m256i)|  
|[_mm256_add_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_add_pd(\__m256d,\__m256d)|  
|[_mm256_add_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_add_ps(\__m256,\__m256)|  
|[_mm256_adds_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_adds_epi16(\__m256i,\__m256i)|  
|[_mm256_adds_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_adds_epi8(\__m256i,\__m256i)|  
|[_mm256_adds_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_adds_epu16(\__m256i,\__m256i)|  
|[_mm256_adds_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_adds_epu8(\__m256i,\__m256i)|  
|[_mm256_addsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_addsub_pd(\__m256d,\__m256d)|  
|[_mm256_addsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_addsub_ps(\__m256,\__m256)|  
|[_mm256_alignr_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_alignr_epi8(\__m256i,\__m256i,const int)|  
|[_mm256_and_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_and_pd(\__m256d,\__m256d)|  
|[_mm256_and_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_and_ps(\__m256,\__m256)|  
|[_mm256_and_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_and_si256(\__m256i,\__m256i)|  
|[_mm256_andnot_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_andnot_pd(\__m256d,\__m256d)|  
|[_mm256_andnot_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_andnot_ps(\__m256,\__m256)|  
|[_mm256_andnot_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_andnot_si256(\__m256i,\__m256i)|  
|[_mm256_avg_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_avg_epu16(\__m256i,\__m256i)|  
|[_mm256_avg_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_avg_epu8(\__m256i,\__m256i)|  
|[_mm256_blend_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_blend_epi16(\__m256i,\__m256i,const int)|  
|[_mm256_blend_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_blend_epi32(\__m256i,\__m256i,const int)|  
|[_mm256_blend_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_blend_pd(\__m256d,\__m256d,const int)|  
|[_mm256_blend_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_blend_ps(\__m256,\__m256,const int)|  
|[_mm256_blendv_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_blendv_epi8(\__m256i,\__m256i,\__m256i)|  
|[_mm256_blendv_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_blendv_pd(\__m256d,\__m256d,\__m256d)|  
|[_mm256_blendv_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_blendv_ps(\__m256,\__m256,\__m256)|  
|[_mm256_broadcast_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_broadcast_pd(\__m128d const *)|  
|[_mm256_broadcast_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_broadcast_ps(\__m128 const *)|  
|[_mm256_broadcast_sd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_broadcast_sd(double const *)|  
|[_mm256_broadcast_ss](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_broadcast_ss(float const *)|  
|[_mm256_broadcastb_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_broadcastb_epi8 (\__m128i)|  
|[_mm256_broadcastd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_broadcastd_epi32(\__m128i)|  
|[_mm256_broadcastq_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_broadcastq_epi64(\__m128i)|  
|[_mm256_broadcastsd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256d _mm256_broadcastsd_pd(\__m128d)|  
|[_mm256_broadcastsi128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_broadcastsi128_si256(\__m128i)|  
|[_mm256_broadcastss_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256 _mm256_broadcastss_ps(\__m128)|  
|[_mm256_broadcastw_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_broadcastw_epi16(\__m128i)|  
|[_mm256_castpd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_castpd_ps(\__m256d)|  
|[_mm256_castpd_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_castpd_si256(\__m256d)|  
|[_mm256_castpd128_pd256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_castpd128_pd256(\__m128d)|  
|[_mm256_castpd256_pd128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d _mm256_castpd256_pd128(\__m256d)|  
|[_mm256_castps_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_castps_pd(\__m256)|  
|[_mm256_castps_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_castps_si256(\__m256)|  
|[_mm256_castps128_ps256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_castps128_ps256(\__m128)|  
|[_mm256_castps256_ps128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm256_castps256_ps128(\__m256)|  
|[_mm256_castsi128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_castsi128_si256(\__m128i)|  
|[_mm256_castsi256_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_castsi256_pd(\__m256i)|  
|[_mm256_castsi256_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_castsi256_ps(\__m256i)|  
|[_mm256_castsi256_si128](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128i _mm256_castsi256_si128(\__m256i)|  
|_mm256_cmov_si256|XOP [1]|ammintrin.h|__m256i _mm256_cmov_si256(\__m256i,\__m256i,\__m256i)|  
|[_mm256_cmp_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d  _mm256_cmp_pd(\__m256d,\__m256d,const int)|  
|[_mm256_cmp_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256  _mm256_cmp_ps(\__m256,\__m256,const int)|  
|[_mm256_cmpeq_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpeq_epi16(\__m256i,\__m256i)|  
|[_mm256_cmpeq_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpeq_epi32(\__m256i,\__m256i)|  
|[_mm256_cmpeq_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpeq_epi64(\__m256i,\__m256i)|  
|[_mm256_cmpeq_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpeq_epi8(\__m256i,\__m256i)|  
|[_mm256_cmpgt_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpgt_epi16(\__m256i,\__m256i)|  
|[_mm256_cmpgt_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpgt_epi32(\__m256i,\__m256i)|  
|[_mm256_cmpgt_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpgt_epi64(\__m256i,\__m256i)|  
|[_mm256_cmpgt_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cmpgt_epi8(\__m256i,\__m256i)|  
|[_mm256_cvtepi16_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepi16_epi32(\__m128i)|  
|[_mm256_cvtepi16_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepi16_epi64(\__m128i)|  
|[_mm256_cvtepi32_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepi32_epi64(\__m128i)|  
|[_mm256_cvtepi32_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_cvtepi32_pd(\__m128i)|  
|[_mm256_cvtepi32_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_cvtepi32_ps(\__m256i)|  
|[_mm256_cvtepi8_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepi8_epi16(\__m128i)|  
|[_mm256_cvtepi8_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepi8_epi32(\__m128i)|  
|[_mm256_cvtepi8_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepi8_epi64(\__m128i)|  
|[_mm256_cvtepu16_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepu16_epi32(\__m128i)|  
|[_mm256_cvtepu16_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepu16_epi64(\__m128i)|  
|[_mm256_cvtepu32_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepu32_epi64(\__m128i)|  
|[_mm256_cvtepu8_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepu8_epi16(\__m128i)|  
|[_mm256_cvtepu8_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepu8_epi32(\__m128i)|  
|[_mm256_cvtepu8_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_cvtepu8_epi64(\__m128i)|  
|[_mm256_cvtpd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128i _mm256_cvtpd_epi32(\__m256d)|  
|[_mm256_cvtpd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm256_cvtpd_ps(\__m256d)|  
|[_mm256_cvtph_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|F16C [2]|immintrin.h|__m256 _mm256_cvtph_ps(\__m128i)|  
|[_mm256_cvtps_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_cvtps_epi32(\__m256)|  
|[_mm256_cvtps_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_cvtps_pd(\__m128)|  
|[_mm256_cvtps_ph](http://go.microsoft.com/fwlink/p/?LinkId=512130)|F16C [2]|immintrin.h|__m128i _mm256_cvtps_ph(\__m256,const int)|  
|[_mm256_cvttpd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128i _mm256_cvttpd_epi32(\__m256d)|  
|[_mm256_cvttps_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_cvttps_epi32(\__m256)|  
|[_mm256_div_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_div_pd(\__m256d,\__m256d)|  
|[_mm256_div_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_div_ps(\__m256,\__m256)|  
|[_mm256_dp_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_dp_ps(\__m256,\__m256,const int)|  
|[_mm256_extractf128_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128d _mm256_extractf128_pd(\__m256d,const int)|  
|[_mm256_extractf128_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128 _mm256_extractf128_ps(\__m256,const int)|  
|[_mm256_extractf128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m128i _mm256_extractf128_si256(\__m256i,const int)|  
|[_mm256_extracti128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm256_extracti128_si256(\__m256i a,int offset)|  
|[_mm256_fmadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256d _mm256_fmadd_pd (\__m256d a,\__m256d b,\__m256d c)|  
|[_mm256_fmadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256 _mm256_fmadd_ps (\__m256 a,\__m256 b,\__m256 c)|  
|[_mm256_fmaddsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256d _mm256_fmaddsub_pd (\__m256d a,\__m256d b,\__m256d c)|  
|[_mm256_fmaddsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256 _mm256_fmaddsub_ps (\__m256 a,\__m256 b,\__m256 c)|  
|[_mm256_fmsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256d _mm256_fmsub_pd (\__m256d a,\__m256d b,\__m256d c)|  
|[_mm256_fmsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256 _mm256_fmsub_ps (\__m256 a,\__m256 b,\__m256 c)|  
|[_mm256_fmsubadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256d _mm256_fmsubadd_pd (\__m256d a,\__m256d b,\__m256d c)|  
|[_mm256_fmsubadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256 _mm256_fmsubadd_ps (\__m256 a,\__m256 b,\__m256 c)|  
|[_mm256_fnmadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256d _mm256_fnmadd_pd (\__m256d a,\__m256d b,\__m256d c)|  
|[_mm256_fnmadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256 _mm256_fnmadd_ps (\__m256 a,\__m256 b,\__m256 c)|  
|[_mm256_fnmsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256d _mm256_fnmsub_pd (\__m256d a,\__m256d b,\__m256d c)|  
|[_mm256_fnmsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|FMA [2]|immintrin.h|__m256 _mm256_fnmsub_ps (\__m256 a,\__m256 b,\__m256 c)|  
|_mm256_frcz_pd|XOP [1]|ammintrin.h|__m256d _mm256_frcz_pd(\__m256d)|  
|_mm256_frcz_ps|XOP [1]|ammintrin.h|__m256 _mm256_frcz_ps(\__m256)|  
|[_mm256_hadd_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_hadd_epi16(\__m256i,\__m256i)|  
|[_mm256_hadd_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_hadd_epi32(\__m256i,\__m256i)|  
|[_mm256_hadd_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_hadd_pd(\__m256d,\__m256d)|  
|[_mm256_hadd_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_hadd_ps(\__m256,\__m256)|  
|[_mm256_hadds_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_hadds_epi16(\__m256i,\__m256i)|  
|[_mm256_hsub_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_hsub_epi16(\__m256i,\__m256i)|  
|[_mm256_hsub_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_hsub_epi32(\__m256i,\__m256i)|  
|[_mm256_hsub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_hsub_pd(\__m256d,\__m256d)|  
|[_mm256_hsub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_hsub_ps(\__m256,\__m256)|  
|[_mm256_hsubs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_hsubs_epi16(\__m256i,\__m256i)|  
|[_mm256_i32gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_i32gather_epi32(int const *base,\__m256i index,const int scale)|  
|[_mm256_i32gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_i32gather_epi64(\__int64 const *base,\__m128i index,const int scale)|  
|[_mm256_i32gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256d _mm256_i32gather_pd(double const *base,\__m128i index,const int scale)|  
|[_mm256_i32gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256 _mm256_i32gather_ps(float const *base,\__m256i index,const int scale)|  
|[_mm256_i64gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_i64gather_epi32(int const *base,\__m256i index,const int scale)|  
|[_mm256_i64gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_i64gather_epi64(\__int64 const *base,\__m256i index,const int scale)|  
|[_mm256_i64gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256d _mm256_i64gather_pd(double const *base,\__m256i index,const int scale)|  
|[_mm256_i64gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm256_i64gather_ps(float const *base,\__m256i index,const int scale)|  
|[_mm256_insertf128_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_insertf128_pd(\__m256d,\__m128d,int )|  
|[_mm256_insertf128_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_insertf128_ps(\__m256,\__m128,int )|  
|[_mm256_insertf128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_insertf128_si256(\__m256i,\__m128i,int )|  
|[_mm256_inserti128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_inserti128_si256(\__m256i,\__m128i,int)|  
|[_mm256_lddqu_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_lddqu_si256(\__m256i *)|  
|[_mm256_load_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_load_pd(double const *)|  
|[_mm256_load_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_load_ps(float const *)|  
|[_mm256_load_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_load_si256(\__m256i *)|  
|[_mm256_loadu_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_loadu_pd(double const *)|  
|[_mm256_loadu_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_loadu_ps(float const *)|  
|[_mm256_loadu_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_loadu_si256(\__m256i *)|  
|_mm256_macc_pd|FMA4 [1]|ammintrin.h|__m256d _mm_macc_pd(\__m256d,\__m256d,\__m256d)|  
|_mm256_macc_ps|FMA4 [1]|ammintrin.h|__m256 _mm_macc_ps(\__m256,\__m256,\__m256)|  
|[_mm256_madd_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_madd_epi16(\__m256i,\__m256i)|  
|_mm256_maddsub_pd|FMA4 [1]|ammintrin.h|__m256d _mm_maddsub_pd(\__m256d,\__m256d,\__m256d)|  
|_mm256_maddsub_ps|FMA4 [1]|ammintrin.h|__m256 _mm_maddsub_ps(\__m256,\__m256,\__m256)|  
|[_mm256_maddubs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_maddubs_epi16(\__m256i,\__m256i)|  
|[_mm256_mask_i32gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mask_i32gather_epi32(\__m256i src,int const *base,\__m256i index,\__m256i mask,const int scale)|  
|[_mm256_mask_i32gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mask_i32gather_epi64(\__m256i src,\__int64 const *base,\__m128i index,\__m256i mask,const int scale)|  
|[_mm256_mask_i32gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256d _mm256_mask_i32gather_pd(\__m256d src,double const *base,\__m128i index,\__m256d mask,const int scale)|  
|[_mm256_mask_i32gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256 _mm256_mask_i32gather_ps(\__m256 src,float const *base,\__m256i index,\__m256 mask,const int scale)|  
|[_mm256_mask_i64gather_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128i _mm256_mask_i64gather_epi32(\__m128i src,int const *base,\__m256i index,\__m128i mask,const int scale)|  
|[_mm256_mask_i64gather_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mask_i64gather_epi64(\__m256i src,\__int64 const *base,\__m256i index,\__m256i mask,const int scale)|  
|[_mm256_mask_i64gather_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256d _mm256_mask_i64gather_pd(\__m256d src,double const *base,\__m256i index,\__m256d mask,const int scale)|  
|[_mm256_mask_i64gather_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m128 _mm256_mask_i64gather_ps(\__m128 src,float const *base,\__m256i index,\__m128 mask,const int scale)|  
|[_mm256_maskload_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_maskload_epi32(int const *,\__m256i)|  
|[_mm256_maskload_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_maskload_epi64( \__int64 const *,\__m256i)|  
|[_mm256_maskload_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_maskload_pd(double const *,\__m256i)|  
|[_mm256_maskload_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_maskload_ps(float const *,\__m256i)|  
|[_mm256_maskstore_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|void _mm256_maskstore_epi32(int *,\__m256i,\__m256i)|  
|[_mm256_maskstore_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|void _mm256_maskstore_epi64(\__int64 *,\__m256i,\__m256i)|  
|[_mm256_maskstore_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_maskstore_pd(double *,\__m256i,\__m256d)|  
|[_mm256_maskstore_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_maskstore_ps(float *,\__m256i,\__m256)|  
|[_mm256_max_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_max_epi16(\__m256i,\__m256i)|  
|[_mm256_max_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_max_epi32(\__m256i,\__m256i)|  
|[_mm256_max_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_max_epi8(\__m256i,\__m256i)|  
|[_mm256_max_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_max_epu16(\__m256i,\__m256i)|  
|[_mm256_max_epu32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_max_epu32(\__m256i,\__m256i)|  
|[_mm256_max_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_max_epu8(\__m256i,\__m256i)|  
|[_mm256_max_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_max_pd(\__m256d,\__m256d)|  
|[_mm256_max_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_max_ps(\__m256,\__m256)|  
|[_mm256_min_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_min_epi16(\__m256i,\__m256i)|  
|[_mm256_min_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_min_epi32(\__m256i,\__m256i)|  
|[_mm256_min_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_min_epi8(\__m256i,\__m256i)|  
|[_mm256_min_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_min_epu16(\__m256i,\__m256i)|  
|[_mm256_min_epu32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_min_epu32(\__m256i,\__m256i)|  
|[_mm256_min_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_min_epu8(\__m256i,\__m256i)|  
|[_mm256_min_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_min_pd(\__m256d,\__m256d)|  
|[_mm256_min_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_min_ps(\__m256,\__m256)|  
|[_mm256_movedup_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_movedup_pd(\__m256d)|  
|[_mm256_movehdup_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_movehdup_ps(\__m256)|  
|[_mm256_moveldup_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_moveldup_ps(\__m256)|  
|[_mm256_movemask_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|int _mm256_movemask_epi8(\__m256i)|  
|[_mm256_movemask_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_movemask_pd(\__m256d)|  
|[_mm256_movemask_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_movemask_ps(\__m256)|  
|[_mm256_mpsadbw_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mpsadbw_epu8(\__m256i,\__m256i,const int)|  
|_mm256_msub_pd|FMA4 [1]|ammintrin.h|__m256d _mm_msub_pd(\__m256d,\__m256d,\__m256d)|  
|_mm256_msub_ps|FMA4 [1]|ammintrin.h|__m256 _mm_msub_ps(\__m256,\__m256,\__m256)|  
|_mm256_msubadd_pd|FMA4 [1]|ammintrin.h|__m256d _mm_msubadd_pd(\__m256d,\__m256d,\__m256d)|  
|_mm256_msubadd_ps|FMA4 [1]|ammintrin.h|__m256 _mm_msubadd_ps(\__m256,\__m256,\__m256)|  
|[_mm256_mul_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mul_epi32(\__m256i,\__m256i)|  
|[_mm256_mul_epu32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mul_epu32(\__m256i,\__m256i)|  
|[_mm256_mul_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_mul_pd(\__m256d,\__m256d)|  
|[_mm256_mul_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_mul_ps(\__m256,\__m256)|  
|[_mm256_mulhi_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mulhi_epi16(\__m256i,\__m256i)|  
|[_mm256_mulhi_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mulhi_epu16(\__m256i,\__m256i)|  
|[_mm256_mulhrs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mulhrs_epi16(\__m256i,\__m256i)|  
|[_mm256_mullo_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mullo_epi16(\__m256i,\__m256i)|  
|[_mm256_mullo_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_mullo_epi32(\__m256i,\__m256i)|  
|_mm256_nmacc_pd|FMA4 [1]|ammintrin.h|__m256d _mm_nmacc_pd(\__m256d,\__m256d,\__m256d)|  
|_mm256_nmacc_ps|FMA4 [1]|ammintrin.h|__m256 _mm_nmacc_ps(\__m256,\__m256,\__m256)|  
|_mm256_nmsub_pd|FMA4 [1]|ammintrin.h|__m256d _mm_nmsub_pd(\__m256d,\__m256d,\__m256d)|  
|_mm256_nmsub_ps|FMA4 [1]|ammintrin.h|__m256 _mm_nmsub_ps(\__m256,\__m256,\__m256)|  
|[_mm256_or_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_or_pd(\__m256d,\__m256d)|  
|[_mm256_or_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_or_ps(\__m256,\__m256)|  
|[_mm256_or_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_or_si256(\__m256i,\__m256i)|  
|[_mm256_packs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_packs_epi16(\__m256i,\__m256i)|  
|[_mm256_packs_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_packs_epi32(\__m256i,\__m256i)|  
|[_mm256_packus_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_packus_epi16(\__m256i,\__m256i)|  
|[_mm256_packus_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_packus_epi32(\__m256i,\__m256i)|  
|[_mm256_permute_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_permute_pd(\__m256d,int)|  
|[_mm256_permute_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_permute_ps(\__m256,int)|  
|_mm256_permute2_pd|XOP [1]|ammintrin.h|__m256d _mm256_permute2_pd(\__m256d,\__m256d,\__m256i,int)|  
|_mm256_permute2_ps|XOP [1]|ammintrin.h|__m256 _mm256_permute2_ps(\__m256,\__m256,\__m256i,int)|  
|[_mm256_permute2f128_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_permute2f128_pd(\__m256d,\__m256d,int)|  
|[_mm256_permute2f128_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_permute2f128_ps(\__m256,\__m256,int)|  
|[_mm256_permute2f128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_permute2f128_si256(\__m256i,\__m256i,int)|  
|[_mm256_permute2x128_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_permute2x128_si256(\__m256i,\__m256i,const int)|  
|[_mm256_permute4x64_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_permute4x64_epi64 (\__m256i,const int)|  
|[_mm256_permute4x64_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256d _mm256_permute4x64_pd(\__m256d,const int)|  
|[_mm256_permutevar_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_permutevar_pd(\__m256d,\__m256i)|  
|[_mm256_permutevar_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_permutevar_ps(\__m256,\__m256i)|  
|[_mm256_permutevar8x32_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_permutevar8x32_epi32(\__m256i,\__m256i)|  
|[_mm256_permutevar8x32_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256 _mm256_permutevar8x32_ps (\__m256,\__m256i)|  
|[_mm256_rcp_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_rcp_ps(\__m256)|  
|[_mm256_round_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_round_pd(\__m256d,int)|  
|[_mm256_round_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_round_ps(\__m256,int)|  
|[_mm256_rsqrt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_rsqrt_ps(\__m256)|  
|[_mm256_sad_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sad_epu8(\__m256i,\__m256i)|  
|[_mm256_set_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|(__m256i _mm256_set_epi16(short|  
|[_mm256_set_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_set_epi32(int,int,int,int,int,int,int,int)|  
|[_mm256_set_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_set_epi8(char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char,char)|  
|[_mm256_set_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_set_pd(double,double,double,double)|  
|[_mm256_set_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_set_ps(float,float,float,float,float,float,float,float)|  
|[_mm256_set1_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_set1_epi16(short)|  
|[_mm256_set1_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_set1_epi32(int)|  
|[_mm256_set1_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_set1_epi8(char)|  
|[_mm256_set1_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_set1_pd(double)|  
|[_mm256_set1_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_set1_ps(float)|  
|[_mm256_setr_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|(__m256i _mm256_setr_epi16(short|  
|[_mm256_setr_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_setr_epi32(int,int,int,int,int,int,int,int)|  
|[_mm256_setr_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|(__m256i _mm256_setr_epi8(char|  
|[_mm256_setr_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_setr_pd(double,double,double,double)|  
|[_mm256_setr_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_setr_ps(float,float,float,float,float,float,float,float)|  
|[_mm256_setzero_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_setzero_pd(void)|  
|[_mm256_setzero_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_setzero_ps(void)|  
|[_mm256_setzero_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256i _mm256_setzero_si256(void)|  
|[_mm256_shuffle_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_shuffle_epi32(\__m256i,const int)|  
|[_mm256_shuffle_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_shuffle_epi8(\__m256i,\__m256i)|  
|[_mm256_shuffle_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_shuffle_pd(\__m256d,\__m256d,const int)|  
|[_mm256_shuffle_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_shuffle_ps(\__m256,\__m256,const int)|  
|[_mm256_shufflehi_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_shufflehi_epi16(\__m256i,const int)|  
|[_mm256_shufflelo_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_shufflelo_epi16(\__m256i,const int)|  
|[_mm256_sign_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sign_epi16(\__m256i,\__m256i)|  
|[_mm256_sign_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sign_epi32(\__m256i,\__m256i)|  
|[_mm256_sign_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sign_epi8(\__m256i,\__m256i)|  
|[_mm256_sll_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sll_epi16(\__m256i,\__m128i)|  
|[_mm256_sll_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sll_epi32(\__m256i,\__m128i)|  
|[_mm256_sll_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sll_epi64(\__m256i,\__m128i)|  
|[_mm256_slli_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_slli_epi16(\__m256i,int)|  
|[_mm256_slli_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_slli_epi32(\__m256i,int)|  
|[_mm256_slli_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_slli_epi64(\__m256i,int)|  
|[_mm256_slli_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_slli_si256(\__m256i,int)|  
|[_mm256_sllv_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sllv_epi32(\__m256i,\__m256i)|  
|[_mm256_sllv_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sllv_epi64(\__m256i,\__m256i)|  
|[_mm256_sqrt_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_sqrt_pd(\__m256d)|  
|[_mm256_sqrt_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_sqrt_ps(\__m256)|  
|[_mm256_sra_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sra_epi16(\__m256i,\__m128i)|  
|[_mm256_sra_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sra_epi32(\__m256i,\__m128i)|  
|[_mm256_srai_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srai_epi16(\__m256i,int)|  
|[_mm256_srai_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srai_epi32(\__m256i,int)|  
|[_mm256_srav_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srav_epi32(\__m256i,\__m256i)|  
|[_mm256_srl_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srl_epi16(\__m256i,\__m128i)|  
|[_mm256_srl_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srl_epi32(\__m256i,\__m128i)|  
|[_mm256_srl_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srl_epi64(\__m256i,\__m128i)|  
|[_mm256_srli_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srli_epi16(\__m256i,int)|  
|[_mm256_srli_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srli_epi32(\__m256i,int)|  
|[_mm256_srli_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srli_epi64(\__m256i,int)|  
|[_mm256_srli_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srli_si256(\__m256i,int)|  
|[_mm256_srlv_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srlv_epi32(\__m256i,\__m256i)|  
|[_mm256_srlv_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_srlv_epi64(\__m256i,\__m256i)|  
|[_mm256_store_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_store_pd(double *,\__m256d)|  
|[_mm256_store_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_store_ps(float *,\__m256)|  
|[_mm256_store_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_store_si256(\__m256i *,\__m256i)|  
|[_mm256_storeu_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_storeu_pd(double *,\__m256d)|  
|[_mm256_storeu_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_storeu_ps(float *,\__m256)|  
|[_mm256_storeu_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_storeu_si256(\__m256i *,\__m256i)|  
|[_mm256_stream_load_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_stream_load_si256(\__m256i const *)|  
|[_mm256_stream_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void __mm256_stream_pd(double *,\__m256d)|  
|[_mm256_stream_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_stream_ps(float *p,\__m256 a)|  
|[_mm256_stream_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void __mm256_stream_si256(\__m256i *,\__m256i)|  
|[_mm256_sub_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sub_epi16(\__m256i,\__m256i)|  
|[_mm256_sub_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sub_epi32(\__m256i,\__m256i)|  
|[_mm256_sub_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sub_epi64(\__m256i,\__m256i)|  
|[_mm256_sub_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_sub_epi8(\__m256i,\__m256i)|  
|[_mm256_sub_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_sub_pd(\__m256d,\__m256d)|  
|[_mm256_sub_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_sub_ps(\__m256,\__m256)|  
|[_mm256_subs_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_subs_epi16(\__m256i,\__m256i)|  
|[_mm256_subs_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_subs_epi8(\__m256i,\__m256i)|  
|[_mm256_subs_epu16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_subs_epu16(\__m256i,\__m256i)|  
|[_mm256_subs_epu8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_subs_epu8(\__m256i,\__m256i)|  
|[_mm256_testc_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testc_pd(\__m256d,\__m256d)|  
|[_mm256_testc_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testc_ps(\__m256,\__m256)|  
|[_mm256_testc_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testc_si256(\__m256i,\__m256i)|  
|[_mm256_testnzc_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testnzc_pd(\__m256d,\__m256d)|  
|[_mm256_testnzc_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testnzc_ps(\__m256,\__m256)|  
|[_mm256_testnzc_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testnzc_si256(\__m256i,\__m256i)|  
|[_mm256_testz_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testz_pd(\__m256d,\__m256d)|  
|[_mm256_testz_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testz_ps(\__m256,\__m256)|  
|[_mm256_testz_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|int _mm256_testz_si256(\__m256i,\__m256i)|  
|[_mm256_unpackhi_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpackhi_epi16(\__m256i,\__m256i)|  
|[_mm256_unpackhi_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpackhi_epi32(\__m256i,\__m256i)|  
|[_mm256_unpackhi_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpackhi_epi64(\__m256i,\__m256i)|  
|[_mm256_unpackhi_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpackhi_epi8(\__m256i,\__m256i)|  
|[_mm256_unpackhi_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_unpackhi_pd(\__m256d,\__m256d)|  
|[_mm256_unpackhi_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_unpackhi_ps(\__m256,\__m256)|  
|[_mm256_unpacklo_epi16](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpacklo_epi16(\__m256i,\__m256i)|  
|[_mm256_unpacklo_epi32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpacklo_epi32(\__m256i,\__m256i)|  
|[_mm256_unpacklo_epi64](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpacklo_epi64(\__m256i,\__m256i)|  
|[_mm256_unpacklo_epi8](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_unpacklo_epi8(\__m256i,\__m256i)|  
|[_mm256_unpacklo_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_unpacklo_pd(\__m256d,\__m256d)|  
|[_mm256_unpacklo_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_unpacklo_ps(\__m256,\__m256)|  
|[_mm256_xor_pd](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256d _mm256_xor_pd(\__m256d,\__m256d)|  
|[_mm256_xor_ps](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|__m256 _mm256_xor_ps(\__m256,\__m256)|  
|[_mm256_xor_si256](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX2 [2]|immintrin.h|__m256i _mm256_xor_si256(\__m256i,\__m256i)|  
|[_mm256_zeroall](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_zeroall(void)|  
|[_mm256_zeroupper](http://go.microsoft.com/fwlink/p/?LinkId=512130)|AVX [2]|immintrin.h|void _mm256_zeroupper(void)|  
|[__movsb](../intrinsics/movsb.md)||intrin.h|VOID __movsb(IN PBYTE,IN BYTE const *,IN SIZE_T)|  
|[__movsd](../intrinsics/movsd.md)||intrin.h|VOID __movsd(IN PDWORD,IN DWORD const *,IN SIZE_T)|  
|[__movsw](../intrinsics/movsw.md)||intrin.h|VOID __movsw(IN PWORD,IN WORD const *,IN SIZE_T)|  
|_mulx_u32|BMI [2]|immintrin.h|unsigned int _mulx_u32(unsigned int,unsigned int,unsigned int*)|  
|[__nop](../intrinsics/nop.md)||intrin.h|void __nop(void)|  
|__nvreg_restore_fence||intrin.h|void __nvreg_restore_fence(void)|  
|__nvreg_save_fence||intrin.h|void __nvreg_save_fence(void)|  
|[__outbyte](../intrinsics/outbyte.md)||intrin.h|void __outbyte(unsigned short Port,unsigned char Data)|  
|[__outbytestring](../intrinsics/outbytestring.md)||intrin.h|void __outbytestring(unsigned short Port,unsigned char *Buffer,unsigned long Count)|  
|[__outdword](../intrinsics/outdword.md)||intrin.h|void __outdword(unsigned short Port,unsigned long Data)|  
|[__outdwordstring](../intrinsics/outdwordstring.md)||intrin.h|void __outdwordstring(unsigned short Port,unsigned long *Buffer,unsigned long Count)|  
|[__outword](../intrinsics/outword.md)||intrin.h|void __outword(unsigned short Port,unsigned short Data)|  
|[__outwordstring](../intrinsics/outwordstring.md)||intrin.h|void __outwordstring(unsigned short Port,unsigned short *Buffer,unsigned long Count)|  
|[_pdep_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI [2]|immintrin.h|unsigned int _pdep_u32(unsigned int,unsigned int)|  
|[_pext_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI [2]|immintrin.h|unsigned int _pext_u32(unsigned int,unsigned int)|  
|[__popcnt](../intrinsics/popcnt16-popcnt-popcnt64.md)|POPCNT|intrin.h|unsigned int __popcnt(unsigned int)|  
|[__popcnt16](../intrinsics/popcnt16-popcnt-popcnt64.md)|POPCNT|intrin.h|unsigned short __popcnt16(unsigned short)|  
|[_rdrand16_step](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RDRAND [2]|immintrin.h|int _rdrand16_step(unsigned short *)|  
|[_rdrand32_step](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RDRAND [2]|immintrin.h|int _rdrand32_step(unsigned int *)|  
|[_rdseed16_step](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RDSEED [2]|immintrin.h|int _rdseed16_step(unsigned short *)|  
|[_rdseed32_step](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RDSEED [2]|immintrin.h|int _rdseed32_step(unsigned int *)|  
|[__rdtsc](../intrinsics/rdtsc.md)||intrin.h|unsigned __int64 \__rdtsc(void)|  
|[__rdtscp](../intrinsics/rdtscp.md)|RDTSCP|intrin.h|unsigned __int64 \__rdtscp(unsigned int*)|  
|[_ReadBarrier](../intrinsics/readbarrier.md)||intrin.h|void _ReadBarrier(void)|  
|[__readcr0](../intrinsics/readcr0.md)||intrin.h|unsigned long __readcr0(void)|  
|[__readcr2](../intrinsics/readcr2.md)||intrin.h|unsigned long __readcr2(void)|  
|[__readcr3](../intrinsics/readcr3.md)||intrin.h|unsigned long __readcr3(void)|  
|[__readcr4](../intrinsics/readcr4.md)||intrin.h|unsigned long __readcr4(void)|  
|[__readcr8](../intrinsics/readcr8.md)||intrin.h|unsigned long __readcr8(void)|  
|[__readdr](../intrinsics/readdr.md)||intrin.h|unsigned __readdr(unsigned)|  
|[__readeflags](../intrinsics/readeflags.md)||intrin.h|unsigned __readeflags(void)|  
|[__readfsbyte](../intrinsics/readfsbyte-readfsdword-readfsqword-readfsword.md)||intrin.h|unsigned char __readfsbyte(unsigned long Offset)|  
|[__readfsdword](../intrinsics/readfsbyte-readfsdword-readfsqword-readfsword.md)||intrin.h|unsigned long __readfsdword(unsigned long Offset)|  
|[__readfsword](../intrinsics/readfsbyte-readfsdword-readfsqword-readfsword.md)||intrin.h|unsigned short __readfsword(unsigned long Offset)|  
|[__readmsr](../intrinsics/readmsr.md)||intrin.h|unsigned __int64 \__readmsr(unsigned long)|  
|[__readpmc](../intrinsics/readpmc.md)||intrin.h|unsigned __int64 \__readpmc(unsigned long a)|  
|[_ReadWriteBarrier](../intrinsics/readwritebarrier.md)||intrin.h|void _ReadWriteBarrier(void)|  
|[_ReturnAddress](../intrinsics/returnaddress.md)||intrin.h|void * _ReturnAddress(void)|  
|_rorx_u32|BMI [2]|immintrin.h|unsigned int _rorx_u32(unsigned int,const unsigned int)|  
|[_rotl16](../intrinsics/rotl8-rotl16.md)||intrin.h|unsigned short _rotl16(unsigned short value,unsigned char shift)|  
|[_rotl8](../intrinsics/rotl8-rotl16.md)||intrin.h|unsigned char _rotl8(unsigned char value,unsigned char shift)|  
|[_rotr16](../intrinsics/rotr8-rotr16.md)||intrin.h|unsigned short _rotr16(unsigned short value,unsigned char shift)|  
|[_rotr8](../intrinsics/rotr8-rotr16.md)||intrin.h|unsigned char _rotr8(unsigned char value,unsigned char shift)|  
|_rsm||intrin.h|void _rsm(void)|  
|_sarx_i32|BMI [2]|immintrin.h|int _sarx_i32(int,unsigned int)|  
|[__segmentlimit](../intrinsics/segmentlimit.md)||intrin.h|unsigned long __segmentlimit(unsigned long a)|  
|_sgdt||intrin.h|void _sgdt(void*)|  
|_shlx_u32|BMI [2]|immintrin.h|unsigned int _shlx_u32(unsigned int,unsigned int)|  
|_shrx_u32|BMI [2]|immintrin.h|unsigned int _shrx_u32(unsigned int,unsigned int)|  
|[__sidt](../intrinsics/sidt.md)||intrin.h|void __sidt(void*)|  
|__slwpcb|LWP [1]|ammintrin.h|void *__slwpcb(void)|  
|_stac|SMAP|intrin.h|void _stac(void)|  
|_store_be_u16<br /><br /> [_storebe_i16](https://software.intel.com/sites/landingpage/IntrinsicsGuide/#text=_storebe_i16&expand=5141)|MOVBE|immintrin.h|void _store_be_u16(void *, unsigned short);<br /><br /> void _storebe_i16(void \*, short); [3]|  
|_store_be_u32<br /><br /> [_storebe_i32](https://software.intel.com/sites/landingpage/IntrinsicsGuide/#text=_storebe_i32&expand=5142)|MOVBE|immintrin.h|void _store_be_u32(void *, unsigned int);<br /><br /> void _storebe_i32(void \*, int); [3]|  
|_Store_HLERelease|HLE [2]|immintrin.h|void _Store_HLERelease(long volatile *,long)|  
|_StorePointer_HLERelease|HLE [2]|immintrin.h|void _StorePointer_HLERelease(void * volatile \*,void \*)|  
|[__stosb](../intrinsics/stosb.md)||intrin.h|void __stosb(IN PBYTE,IN BYTE,IN SIZE_T)|  
|[__stosd](../intrinsics/stosd.md)||intrin.h|void __stosd(IN PDWORD,IN DWORD,IN SIZE_T)|  
|[__stosw](../intrinsics/stosw.md)||intrin.h|void __stosw(IN PWORD,IN WORD,IN SIZE_T)|  
|_subborrow_u16||intrin.h|unsigned char _subborrow_u16(unsigned char b_in,unsigned short src1,unsigned short src2,unsigned short *diff)|  
|[_subborrow_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)||intrin.h|unsigned char _subborrow_u32(unsigned char b_in,unsigned int src1,unsigned int src2,unsigned int *diff)|  
|_subborrow_u8||intrin.h|unsigned char _subborrow_u8(unsigned char b_in,unsigned char src1,unsigned char src2,unsigned char *diff)|  
|[__svm_clgi](../intrinsics/svm-clgi.md)||intrin.h|void __svm_clgi(void)|  
|[__svm_invlpga](../intrinsics/svm-invlpga.md)||intrin.h|void __svm_invlpga(void*,int)|  
|[__svm_skinit](../intrinsics/svm-skinit.md)||intrin.h|void __svm_skinit(int)|  
|[__svm_stgi](../intrinsics/svm-stgi.md)||intrin.h|void __svm_stgi(void)|  
|[__svm_vmload](../intrinsics/svm-vmload.md)||intrin.h|void __svm_vmload(size_t)|  
|[__svm_vmrun](../intrinsics/svm-vmrun.md)||intrin.h|void __svm_vmrun(size_t)|  
|[__svm_vmsave](../intrinsics/svm-vmsave.md)||intrin.h|void __svm_vmsave(size_t)|  
|_t1mskc_u32|ABM [1]|ammintrin.h|unsigned int _t1mskc_u32(unsigned int)|  
|[_tzcnt_u32](http://go.microsoft.com/fwlink/p/?LinkId=512130)|BMI|ammintrin.h, immintrin.h|unsigned int _tzcnt_u32(unsigned int)|  
|_tzmsk_u32|ABM [1]|ammintrin.h|unsigned int _tzmsk_u32(unsigned int)|  
|[__ud2](../intrinsics/ud2.md)||intrin.h|void __ud2(void)|  
|[__ull_rshift](../intrinsics/ull-rshift.md)||intrin.h|unsigned __int64 [pascal/cdecl] \__ull_rshift(unsigned \__int64,int)|  
|[__vmx_off](../intrinsics/vmx-off.md)||intrin.h|void __vmx_off(void)|  
|[__vmx_vmptrst](../intrinsics/vmx-vmptrst.md)||intrin.h|void __vmx_vmptrst(unsigned \__int64 *)|  
|[__wbinvd](../intrinsics/wbinvd.md)||intrin.h|void __wbinvd(void)|  
|[_WriteBarrier](../intrinsics/writebarrier.md)||intrin.h|void _WriteBarrier(void)|  
|[__writecr0](../intrinsics/writecr0.md)||intrin.h|void __writecr0(unsigned long)|  
|[__writecr3](../intrinsics/writecr3.md)||intrin.h|void __writecr3(unsigned long)|  
|[__writecr4](../intrinsics/writecr4.md)||intrin.h|void __writecr4(unsigned long)|  
|[__writecr8](../intrinsics/writecr8.md)||intrin.h|void __writecr8(unsigned long)|  
|[__writedr](../intrinsics/writedr.md)||intrin.h|void __writedr(unsigned,unsigned)|  
|[__writeeflags](../intrinsics/writeeflags.md)||intrin.h|void __writeeflags(unsigned)|  
|[__writefsbyte](../intrinsics/writefsbyte-writefsdword-writefsqword-writefsword.md)||intrin.h|void __writefsbyte(unsigned long Offset,unsigned char Data)|  
|[__writefsdword](../intrinsics/writefsbyte-writefsdword-writefsqword-writefsword.md)||intrin.h|void __writefsdword(unsigned long Offset,unsigned long Data)|  
|[__writefsword](../intrinsics/writefsbyte-writefsdword-writefsqword-writefsword.md)||intrin.h|void __writefsword(unsigned long Offset,unsigned short Data)|  
|[__writemsr](../intrinsics/writemsr.md)||intrin.h|void __writemsr(unsigned long,unsigned \__int64)|  
|[_xabort](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RTM [2]|immintrin.h|void _xabort(unsigned int)|  
|[_xbegin](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RTM [2]|immintrin.h|unsigned _xbegin(void)|  
|[_xend](http://go.microsoft.com/fwlink/p/?LinkId=512130)|RTM [2]|immintrin.h|void _xend(void)|  
|[_xgetbv](http://go.microsoft.com/fwlink/p/?LinkId=512130)|XSAVE [2]|immintrin.h|unsigned __int64 _xgetbv(unsigned int)|  
|[_xrstor](http://go.microsoft.com/fwlink/p/?LinkId=512130)|XSAVE [2]|immintrin.h|void _xrstor(void const*,unsigned \__int64)|  
|[_xsave](http://go.microsoft.com/fwlink/p/?LinkId=512130)|XSAVE [2]|immintrin.h|void _xsave(void*,unsigned \__int64)|  
|[_xsaveopt](http://go.microsoft.com/fwlink/p/?LinkId=512130)|XSAVEOPT [2]|immintrin.h|void _xsaveopt(void*,unsigned \__int64)|  
|[_xsetbv](http://go.microsoft.com/fwlink/p/?LinkId=512130)|XSAVE [2]|immintrin.h|void _xsetbv(unsigned int,unsigned \__int64)|  
|[_xtest](http://go.microsoft.com/fwlink/p/?LinkId=512130)|XTEST [2]|immintrin.h|unsigned char _xtest(void)|  
  
## See Also  
 [Compiler Intrinsics](../intrinsics/compiler-intrinsics.md)   
 [ARM Intrinsics](../intrinsics/arm-intrinsics.md)   
 [x64 (amd64) Intrinsics](../intrinsics/x64-amd64-intrinsics-list.md)