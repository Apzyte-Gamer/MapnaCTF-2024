XXG
=

Welcome to the Forensics [XXG](https://mapnactf.com/tasks/MAPNA.XXG_04de6faaebbf29fb11639ef77530d3b85f09a2ce.txz) challenge! Our investigator stumbled upon a mysterious file. Can you uncover the hidden message?

Solution
=

Upon opening the file, I noticed the file format at the top was written as PNG. I converted the file to a PNG but it only displayed an image having the text `MAPNA`.
Therefore, I reverted my changes and went on to a hex-editor ([010](https://www.sweetscape.com/010editor/)) and looked in the strings.

Upon scrolling and reading carefully, I stumbled upon this particular text that caught my eye:

```
Gi?? ??? v014ÈúBBõ????-image-grid¬(style solid)
(fgcolor (color-rgba 0 0 0 1))
(bgcolor (color-rgba 1 1 1 1))
(xspacing 10)
(yspacing 10)
(spacing-unit inches)
(xoffset 0)
(yoffset 0)
(offset-unit inches)
gamma0.45455000000000001gimp-image-metadataç<?xml version='1.0' encoding='UTF-8'?>
<metadata>
  <tag name="Exif.Image.BitsPerSample">16 16 16</tag>
  <tag name="Exif.Image.ImageLength">12</tag>
  <tag name="Exif.Image.ImageWidth">200</tag>
  <tag name="Exif.Image.Orientation">1</tag>
  <tag name="Exif.Image.ResolutionUnit">2</tag>
  <tag name="Exif.Image.XResolution">300/1</tag>
  <tag name="Exif.Image.YResolution">300/1</tag>
  <tag name="Exif.Photo.ColorSpace">1</tag>
  <tag name="Xmp.tiff.Orientation">1</tag>
</metadata>
lÈ	????.???ÿ!?	"
 
%$ÿÿÿÿ#ÿÿÿÿuÈ¡amÈÑMáÿçãÏÿÿì¿ÿÿ]¦ÿÿã VFÂãäÿÿKÿþ]¦ÿê³EÖSS¯ÕS[V÷ãSS¯ðRPDÔÿÞOMÿã=uÿÿA¿ÿôUTÿÿã_ÿî=ã<OÿÿKÿÿôUTÿüZßã_ÿùðóÿ¬ã_ÿþÿ×=ÿqÿãlCþÿS}¿ÿ¢ Wéÿã_ÿÿ=ãqZªÿKÿÿ¢ WéÿÿIðã_ÿü¹ã_ÿý¸VôÿÅa¦?ÿãkÁáo¿ÿLðªÿã_ÿÏWãlæ%îKÿÿLðªÿvuÿã WWÎÿÿäFüã WWÎÿ 5üÿ×	¿ÿãkÙhÉ¿åOJ:ÿã VhéãkÿbNÿåOJ:ÿÿKöã_ÿúñIàÿã_ÿýýlÿë¯má>ÿãkÿGNÿ¿²ÿÿ]×ã_ÿîãkÿû+*ÿ²ÿÿ]×ÿWçã_ÿùøRÒÿÿã_ÿûþÿÿ¦ÿë®ÿáÿãkÿ~ÿ¿Dûÿÿ¼zã_ÿîãkÿÿ¾ÿDûÿÿ¼zÿeÎã_ÿù&KKã_ÿûIUZóÿüèSk^!ÿýÙVðQÿÿýkÿùBÿÿçãÏÿÿì¿ÿÿ]¦ÿÿã VFÂãäÿÿKÿþ]¦ÿê³E{SS¯ÕS[V÷ãSS¯ðRPDÔÿÞOMÿã=uÿÿA¿ÿôUTÿÿã_ÿî=ã<OÿÿKÿÿôUTÿüZßã_ÿùðóÿ¬ã_ÿþÿ×=ÿqÿãlCþÿS}¿ÿ¢ Wéÿã_ÿÿ=ãqZªÿKÿÿ¢ WéÿÿIðã_ÿü¹ã_ÿý¸VôÿÅa¦?ÿãkÁáo¿ÿLðªÿã_ÿÏWãlæ%îKÿÿLðªÿvuÿã WWÎÿÿäFüã WWÎÿ 5üÿ×	¿ÿãkÙhÉ¿åOJ:ÿã VhéãkÿbNÿåOJ:ÿÿKöã_ÿúñIàÿã_ÿýýlÿë¯má>ÿãkÿGNÿ¿²ÿÿ]×ã_ÿîãkÿû+*ÿ²ÿÿ]×ÿWçã_ÿùøRÒÿÿã_ÿûþÿÿ¦ÿë®ÿáÿãkÿ~ÿ¿Dûÿÿ¼zã_ÿîãkÿÿ¾ÿDûÿÿ¼zÿeÎã_ÿù&KKã_ÿûIUZóÿüèSk^!ÿýÙVðQÿÿýkÿùBÿÿÿ÷ÿðã XNÿãSS¯ðRPDÔÿ÷saÊÑ"Ûÿã_ÿûÇP[Pòÿöò OOáGäÿëBÿþÆÿøã_ÿÿ?ïã_ÿþÿöþEÿ÷_hÛÿã_ÿûñúÿ¢ÿþárÿû½gÿqµÿÿóÿøã_ÿüCøã_ÿý¸VôÿöuÿÿoÛÿã_ÿýþgÁÿþÐÿôAÀ>ÿÊN]ÿÿ×ùÿðã W.ÿã WWÎÿ 5üÿþûGÿûoÛÿã_ÿü>VùÿôÎE_jñÿº	·ÿ¥ÿýØDþÿøã_ÿþYÏã_ÿýýlÿþûGÿûoÛÿã_ÿþ¦ÿò®|ÿÿ4ÿÿùPÂÿÿøã_ÿÿjÀã_ÿûþÿÿ¦ÿþûGÿûoÛÿã_ÿûýÿÿºxÿû¿{ÿÿ?ÿúõ@ÿAÚÿøã WPfýã_ÿûIUZóÿþûGÿóoÛÿãOO­S\Uéÿò·X]Yìÿÿ?ÿÿ¥Z[Bÿÿýkÿù
ÿÿýkÿùÿÿýkÿùMÿÿÿ÷ÿðã XNÿãSS¯ðRPDÔÿ÷saÊÑ"Ûÿã_ÿûÇP[Pòÿöò OOáGäÿëBÿþÆÿøã_ÿÿ?ïã_ÿþÿöþEÿ÷_hÛÿã_ÿûñúÿ¢ÿþárÿû½gÿqµÿÿóÿøã_ÿüCøã_ÿý¸VôÿöuÿÿoÛÿã_ÿýþgÁÿþÐÿôAÀ>ÿÊN]ÿÿ×ùÿðã W.ÿã WWÎÿ 5üÿþûGÿûoÛÿã_ÿü>VùÿôÎE_jñÿº	·ÿ¥ÿýØDþÿøã_ÿþYÏã_ÿýýlÿþûGÿûoÛÿã_ÿþ¦ÿò®|ÿÿ4ÿÿùPÂÿÿøã_ÿÿjÀã_ÿûþÿÿ¦ÿþûGÿûoÛÿã_ÿûýÿÿºxÿû¿{ÿÿ?ÿúõ@ÿAÚÿøã WPfýã_ÿûIUZóÿþûGÿóoÛÿãOO­S\Uéÿò·X]Yìÿÿ?ÿÿ¥Z[Bÿÿýkÿù
ÿÿýkÿùÿÿýkÿùMÿÿOñDXÇP[PòãÏÿÿì¿	ÿýä
ûÿûãSS¯ÿ÷ãäÿÿKÿÑÿçÇP[PòxWGÿÿ¯ñúÿ¢ã=uÿÿA¿	ÿýfBûÿþã_ÿúã<OÿÿKÿãñúÿ¢þÿÚÿÿDüÿÿþgÁãlCþÿS}¿ÊN]ÿöÃQûÇqT§ã_ÿØãqZªÿKÿÇýeVfÿÿþgÁÿÿÿºÿÿ>VùãkÁáo¿¥ÿòýSøOûÇCþÿã WWÎÿõãlæ%îKÿÇ®ÿö>Vùÿ¸pÿRåÿò¦ãkÙhÉ¿ùPÂÿõ±ÿOûÇ}ÿÿã_ÿõãkÿbNÿÇ´ÿæ¦ÿeýßVÿÿýÿÿºxãkÿGNÿ¿ÿÿõ@ÿõTOOTÇÿÿã_ÿÖãkÿû+*ÿÇ«ÿÿýÿÿºxÿâÿu»ÿÿS\Uéãkÿ~ÿ¿¥Z[ÿõOûÇÿÿãOO­ÿëãkÿÿ¾ÿÇübU[S\Uéÿ3öSÿÿýkÿùÿÿýkÿùSÿÿOñDXÇP[PòãÏÿÿì¿	ÿýä
ûÿûãSS¯ÿ÷ãäÿÿKÿÑÿçÇP[PòxWGÿÿ¯ñúÿ¢ã=uÿÿA¿	ÿýfBûÿþã_ÿúã<OÿÿKÿãñúÿ¢þÿÚÿÿDüÿÿþgÁãlCþÿS}¿ÊN]ÿöÃQûÇqT§ã_ÿØãqZªÿKÿÇýeVfÿÿþgÁÿÿÿºÿÿ>VùãkÁáo¿¥ÿòýSøOûÇCþÿã WWÎÿõãlæ%îKÿÇ®ÿö>Vùÿ¸pÿRåÿò¦ãkÙhÉ¿ùPÂÿõ±ÿOûÇ}ÿÿã_ÿõãkÿbNÿÇ´ÿæ¦ÿeýßVÿÿýÿÿºxãkÿGNÿ¿ÿÿõ@ÿõTOOTÇÿÿã_ÿÖãkÿû+*ÿÇ«ÿÿýÿÿºxÿâÿu»ÿÿS\Uéãkÿ~ÿ¿¥Z[ÿõOûÇÿÿãOO­ÿëãkÿÿ¾ÿÇübU[S\Uéÿ3öSÿÿýkÿùÿÿýkÿùSÿÿûÌÄ^cÿâkÐiÿDöÿÿÜuÿRèÿÿþèÿ®-èÿÿöªÿáÿûûêÿPóÿûÄaÿGûÿþÿÿûÌÄ^cÿâkÐiÿDöÿÿÜuÿRèÿÿþèÿ®-èÿÿöªÿáÿûûêÿPóÿûÄaÿGûÿþÿd2
```
