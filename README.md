# Lab.3

利用正規表示法撰寫程式碼來分析 HTML 檔案中的文字敘述部分，並將分析結果寫檔。
分析規則如下：

* 遇到
** <DIV>
** <P>
** <BR>
  需換行
* 遇到超連結，需將連結顯示的字串輸出，舉例來說若是
 ```
 <a href="http://forums.au.reachout.com/t5/user/viewprofilepage/user-id/5937">@lanejane</a>
 ```
 則顯示
 ```
 @lanejane
 ```
* 遇到圖形，則把 title 的字輸出；舉例來說若是
 ```
 <img class="emoticon emoticon-smileyhappy" id="smileyhappy" src="http://inspire.i.lithium.com/i/smilies/16x16_smiley-happy.png" alt="Smiley Happy" title="Smiley Happy" />
 ```
 則需輸出
 ```
 Smiley Happy
 ```

## Example

```
Re: Turning Negatives Into Positives
<p/>
<P><STRONG>Neg</STRONG>: Things at home are overwhelming me today. I can't even type properly right now. Feeling so very overwhelmed so annoyed. Feeilng at the end of my tether</P>
<P><STRONG>Pos</STRONG>: I'm aware that things are hitting my limit. I am working towards being open with my psych. I am giong to do some relaxation exercises tonight after this, really just try to calm. I'm tryig to focus on the youtube mix I'm listening to right now</P>
```

```
Re: Turning Negatives Into Positives
Neg: Things at home are overwhelming me today. I can't even type properly right now. Feeling so very overwhelmed so annoyed. Feeilng at the end of my tether

Pos: I'm aware that things are hitting my limit. I am working towards being open with my psych. I am giong to do some relaxation exercises tonight after this, really just try to calm. I'm tryig to focus on the youtube mix I'm listening to right now
```