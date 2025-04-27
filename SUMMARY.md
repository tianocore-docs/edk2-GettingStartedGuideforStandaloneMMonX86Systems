<!--- @file
  Summary

  Copyright (c) 2025, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

-->

# Summary

* [Standalone MM Getting Started Guide](README.md)

* [MM Introduction](1_mm_introduction.md#mm-introduction)
  * [SMM and MM Overview](1_mm_introduction.md#smm-and-mm-overview)
  * [MM Driver Dispatch](1_mm_introduction.md#mm-driver-dispatch)
  * [MM Communication Buffer](1_mm_introduction.md#mm-communication-buffer)
  * [Non-MMRAM Access](1_mm_introduction.md#non-mmram-access)
  * [MM HOBs](1_mm_introduction.md#mm-hobs)
    * [MM Foundation HOBs](1_mm_introduction.md#mm-foundation-hobs)
    * [MM Platform HOBs](1_mm_introduction.md#mm-platform-hobs)
  * [Communication between SMM/Non-SMM](1_mm_introduction.md#communication-between-smmnon-smm)
  * [Memory Protection](1_mm_introduction.md#memory-protection)

* [SMM to MM Porting Guide](2_smm_to_mm_porting_guide.md#smm-to-mm-porting-guide)
  * [Porting Design Overview](2_smm_to_mm_porting_guide.md#porting-design-overview)
  * [Checkpoints in Converted MM Driver](2_smm_to_mm_porting_guide.md#checkpoints-in-converted-mm-driver)
  * [Sample: SMM to MM Conversion](2_smm_to_mm_porting_guide.md#sample-smm-to-mm-conversion)

---

* Tables
  * [Table 1 - SMM and MM Memory Protection Policy](1_mm_introduction.md#table-1-smm-and-mm-memory-protection-policy)

---

* Figures
 * [Figure 1 - MM Driver Dispatch Flow](1_mm_introduction.md#figure-1-mm-driver-dispatch-flow)
 * [Figure 2 - SMM to MM Conversion](2_smm_to_mm_porting_guide.md#figure-2-smm-to-mm-conversion)
 * [Figure 3 - Tcg2 SMM and MM Module Type](2_smm_to_mm_porting_guide.md#figure-3-tcg2-smm-and-mm-module-type)
 * [Figure 4 - Tcg2 SMM and MM Entry Point](2_smm_to_mm_porting_guide.md#figure-4-tcg2-smm-and-mm-entry-point)
 * [Figure 5 - Tcg2 HOB to Replace PCD](2_smm_to_mm_porting_guide.md#figure-5-tcg2-hob-to-replace-pcd)
 * [Figure 6 - Tcg2 Primary and Non-Primary Buffer Check](2_smm_to_mm_porting_guide.md#figure-6-tcg2-primary-and-non-primary-buffer-check)
