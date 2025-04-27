<!--- @file
  Second Chapter of EDK II Template Specification

  Copyright (c) 2017 - 2020, Intel Corporation. All rights reserved.<BR>

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

# 2 Second Chapter

This is a really short paragraph.

This is another paragraph.

## 2.1 List Items

*Not a list item. A list item requires a least once space.

* Hello 
*  Hello
*   Hello
*    Hello
  * Hello
  + Hello
      + hello
  - Hello
* [link](#2-second-chapter)
    * Hello
    
## 2.2 Tables

The table below is a simple table with no specified alignment.
    
###### Table 10 - Small Table
|  a  |  b  |  c  |
| --- | --- | --- |
|  1  |  2  |  3  |

The table below is a simple table with example of left, center, and right
alignment.

###### Table 11 - Small Table With Alignment
|  a  |  b  |  c  |
|:--- |:---:| ---:|
|  1  |  2  |  3  |

## 2.3 Code Examples

Single line code example

`This is code style in a single line`

Code block
                                                                                                                                                                                                                        
```
Code example
```
###### Example 27 - Hello world

Code block of C code with color syntax highlighting

```c
UINT8
EFIAPI
DecimalToBcd8 (
  IN      UINT8                     Value
  )
{
  ASSERT (Value < 100);
  return (UINT8) (((Value / 10) << 4) | (Value % 10));
}
```
###### Example 28 - C code example

Code block of INF file. INF files use INI file color syntax highlighting.

```ini
[Defines]
  INF_VERSION                    = 0x00010005
  BASE_NAME                      = BaseLib
  MODULE_UNI_FILE                = BaseLib.uni
  FILE_GUID                      = 27d67720-ea68-48ae-93da-a3a074c90e30
  MODULE_TYPE                    = BASE
  VERSION_STRING                 = 1.1
  LIBRARY_CLASS                  = BaseLib 
```
###### Example 29 - INI file example

## 2.4 Figures

The following figure is the Tianocore logo for documents

![](media/TianocoreTitlePageLogo.jpg)
###### Figure 7 - Tianocore Logo
 
The figures below are generated using the PlantUML plugin that uses [PlantUML](http://plantuml.com) syntax that is defined [here](http://plantuml.com/sitemap-language-specification).


{% plantuml %}
@startdot
digraph G {
  a -> b
  b -> c
  c -> a
}
@enddot
{% endplantuml %}

###### Figure 8 - Simple DOT Diagram

{% plantuml %}
@startuml
Class EFI_DISK_IO_PROTOCOL {
  +Revision
  +ReadDisk(This, MediaId, Offset, BufferSize, Buffer)
  +WriteDisk(This, MediaId, Offset, BufferSize, Buffer)
}
Class EFI_BLOCK_IO_PROTOCOL {
  +Revision
  +Media
  +Reset(This, ExtendedVerification)
  +ReadBlocks(This, MediaId, Lba, BufferSize, Buffer)
  +WriteBlock(This, MediaId, Lba, BufferSize, Buffer)
  +FlushBlock(This)
}

Class EFI_BLOCK_IO_MEDIA {
  +MediaId
  +RemovableMedia
  +MediaPresent
  +LogicalPartition
  +ReadOnly
  +WriteCaching
  +BlockSize
  +IoAlign
  +LastBlock
  +LowestAlignedLba
  +LogicalBlocksPerPhysicalBlock
  +OptimalTransferLengthGranularity
} 

together {
  class EFI_BLOCK_IO_PROTOCOL
  class EFI_BLOCK_IO_MEDIA
}
EFI_BLOCK_IO_PROTOCOL - EFI_BLOCK_IO_MEDIA

EFI_DISK_IO_PROTOCOL --> EFI_BLOCK_IO_PROTOCOL
@enduml
{% endplantuml %}

###### Figure 9 - UML Class Diagram

{% plantuml %}
@startdot
digraph G {
  graph [style=rounded]
  subgraph cluster_0 {
    label = "UEFI Objects";
    subgraph column_3 {
      style=invis;
      label = "";
      "Memory" -> "Environment\nvariables" -> "Watchdog\ntimer"[style=invis];
    }
    subgraph column_2 {
      style=invis;
      label = "";
      "Images" -> "Handles\nand\nprotocols" -> "Monotonic\ncounter"[style=invis];
    }
    subgraph column_1 {
      style=invis;
      label = "";
     "UEFI system\ntable" -> "Events" -> "Time / date" [style=invis];
    }
  }
}
@enddot
{% endplantuml %}

###### Figure 10 - DOT Diagram

{% plantuml %}
@startditaa
+---------------------------------------------+
|cGRE                                         |
|      EFI System File System Protocol        |
|                                             |
+----------------------+----------------------+
                       |
                       V
+----------------------+----------------------+
|cBLU                                         |
|           EFI Disk I/O Protocol             |
|                                             |
+----------------------+----------------------+
                       |
                       V
/----------------------+----------------------\
|cYEL                                         |
|           EFI Block I/O Protocol            |
|                                             |
\---------------------------------------------/
@endditaa
{% endplantuml %}

###### Figure 11 - DITAA Diagram


## 2.5 Tips, Notes, Cautions, Warnings
  
*********
**Note:** This is a note.
*********

This is a paragraph between notes

*********
**Note:** This is a multiple line note. This is on first line.

This is on second line.

This is on third line.
*********

This is a paragraph after a note

**********
**Warning:** This is a warning.
**********
**Note:** This is a note immediately after a warning
**********

This is a paragraph after combined warning and note.




