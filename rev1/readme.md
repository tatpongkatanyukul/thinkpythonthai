# แก้ตามความเห็นผู้ทรงคุณวุฒิ

 * หนังสือนำ อว 660201.2.4/406 ลงวันที่ 21 ตค 2564 (เจ้าของเรื่อง วนิดา สุขโข)
 * กำหนดส่ง 25 พย 2564
 * ส่งจริง ?

Latex tricks:
 * ```\newcommand\atom[1]{\noindent\mbox{#1}\noindent}``` sort of a patch for bad thai word segmentation, but then I have to manually apply ```\atom{word}``` to every word I need to keep it intact. Painful! Verdict: don't do latex for thai.
 * ```\index{main!sub}```
   * ทำดัชนีเป็นลำดับชั้น
 * ```\index{join@\textbf{join}}```
   * เปลี่ยนฟอนต์ดัชนี (เน้นจุดที่เป็นหัวข้อหลัก)
 * ```\section[ตารางแฮช]{ตารางแฮช (Hashtables)}```
   * แยกชื่อหัวข้อที่แสดง กับชื่อที่ปรากฎในสารบัญ 
 * compile เป็น latex หรือ html
    * option 1: compile it wiht ```htlatex```, e.g., ```htlatex book.tex``` (see [How to convert latex to html](https://data-mining.philippe-fournier-viger.com/how-to-convert-latex-to-html/))
      * ```htlatex``` seems to have troubles with ```fontspec```, so using ```fontspec``` to handle thai would not allow this option.
 * Put all fonts into pdf (mitigate the issue of font missing during print):
 ```
 C:\"Program Files"\gs\gs9.54.0\bin\gswin64c -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dPDFSETTINGS=/prepress -dEmbedAllFonts=true -sOutputFile=TPrev1b_fixed.pdf -f TPrev1b.pdf
 ```

## แก้ไม่ได้
  * Latex ตัดคำภาษาไทยสุดห่วย ตัองไล่ดู แล้วแก้มือแต่ละบรรทัด ... เจ็บปวดสุด ๆ
    * พอดีกว่า ... เก็บ latex ไว้ใช้กับภาษาอังกฤษดีกว่า
    * แล้วภาษาไทย ใช้อะไร ???? ...
