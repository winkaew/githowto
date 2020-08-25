      *  This document serves as the reference for the Pascal language as implemented by the Free Pascal compiler.
      *  เอกสารนี้ ให้ข้อมูลเรื่องของ ภาษา pascal โดยใช้ Free Pascal compiler.
   * It describes all Pascal constructs supported by Free Pascal, and lists all supported data types. 
   * It does not, however, give a detailed explanation of the Pascal language: it is not a tutorial.
   * The aim is to list which Pascal constructs are supported, 
   *  and to show where the Free Pascal implementation differs from the Turbo Pascal or Delphi implementations. 
   The Turbo Pascal and Delphi Pascal compilers introduced various features in the Pascal language.
   The Free Pascal compiler emulates these compilers in the appropriate mode of the compiler: 
   certain features are available only if the compiler is switched to the appropriate mode. When required for a certain feature,
   the use of the -M command-line switch or {$MODE } directive will be indicated in the text.
   More information about the various modes can be found in the user’s manual and the programmer’s manual. 
   Earlier versions of this document also contained the reference documentation of the system unit and objpas unit.
   This has been moved to the RTL reference guide. 
The language Pascal was originally designed by Niklaus Wirth around 1970. It has evolved significantly since that day, with a lot of contributions by the various compiler constructors (Notably: Borland). The basic elements have been kept throughout the years: 
Easy syntax, rather verbose, yet easy to read. Ideal for teaching. 
Strongly typed. 
Procedural. 
Case insensitive. 
Allows nested procedures. 
Easy input/output routines built-in.
The Turbo Pascal and Delphi Pascal compilers introduced various features in the Pascal language, most notably easier string handling and object orientedness. The Free Pascal compiler initially emulated most of Turbo Pascal and later on Delphi. It emulates these compilers in the appropriate mode of the compiler: certain features are available only if the compiler is switched to the appropriate mode. When required for a certain feature, the use of the -M command-line switch or {$MODE } directive will be indicated in the text. More information about the various modes can be found in the user’s manual and the programmer’s manual. 
[prev] [prev-tail] [front] [up] 
