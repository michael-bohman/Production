# Notes on Pixel Alignment

Alignment software does not support 21216-04 or 21214-03. Need to do some adjusting to make it work.



Easiest is...

1. Go to Sentera OEM configuration.&#x20;
2. May have to adjust some gains (david knows how).
3. Take Focus and Alignment pictures
4. Plug the hw\_config from the programming tech package into the alignment app.
   1. 21214-02 instead of -03
   2. 21216-03 instead of -04
5. Use the output hw\_config and copy alignent specs over to the blank 21214-03 and 21216-04 hw\_configs using something like Beyond Compare.
6. Make sure to set the serial number correctly (with the single quotes around the number)
7. Save new one to camera
8. take alignment test pictures to make sure that it applied correctly
   1. put all into one folder and scroll through quickly to make sure all the IMG\_0001s are aligned, etc...
