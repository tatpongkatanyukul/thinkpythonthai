# แก้ตามความเห็นผู้ทรงคุณวุฒิ

 * หนังสือนำ อว 660201.2.4/406 ลงวันที่ 21 ตค 2564 (เจ้าของเรื่อง วนิดา สุขโข)
 * กำหนดส่ง 25 พย 2564
 * ส่งจริง ?

Latex tricks:
 * ```\index{main!sub}```
   * ทำดัชนีเป็นลำดับชั้น
 * ```\index{join@\textbf{join}}```
   * เปลี่ยนฟอนต์ดัชนี (เน้นจุดที่เป็นหัวข้อหลัก)
 * ```\section[ตารางแฮช]{ตารางแฮช (Hashtables)}```
   * แยกชื่อหัวข้อที่แสดง กับชื่อที่ปรากฎในสารบัญ 
 * compile เป็น latex หรือ html
    * option 1: compile it wiht ```htlatex```, e.g., ```htlatex article.tex``` (see [How to convert latex to html](https://data-mining.philippe-fournier-viger.com/how-to-convert-latex-to-html/))
      * ```htlatex``` seems to have troubles with ```fontspec```, so using ```fontspec``` to handle thai would not allow this option.

 * Put all fonts into pdf (mitigate the issue of font missing during print):
 ```
 C:\"Program Files"\gs\gs9.54.0\bin\gswin64c -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dPDFSETTINGS=/prepress -dEmbedAllFonts=true -sOutputFile=TPrev1b_fixed.pdf -f TPrev1b.pdf
 ```
