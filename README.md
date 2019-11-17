# 06_csa
# 「社區共購小幫手」

「社區共購小幫手」團隊以最佳、最優先維繫「社區共購、集購熱度的現場場景」的理念，發展獨特的社群銷售應用，解決傳統上科技應用無視使用者脈絡，易導致服務失靈的問題（例如近年的無人科技商店銷售低落問題）。

* 「+1留言即訂單」：社群熱度當下回文留言「＋1」或「+N」即視為訂單成立，待收單結購時，將所有貼文全數複製至表單系統中即完成全部訂單輸入，每筆留言＋1均視為「留言單」。
* 「留言單文字扒單」：在任一試算表工具(如：Google Sheets, MS Excel, LibreOffice Calc等)中，憑以下「留言單」關鍵字疏理(以vba語法撰寫)資料行程式即可運作。
* 訂購資料行程式

```
=iferror(if(find("+",A3)<>"#VALUE!",A3,0),"")
```

* 訂購人及訂購量行程式

```
=SPLIT(C3,"+")
```

* 匯整訂購人及訂單明細程式

```
=sort(D3:E741,1,false)
```

* 總單數結算行程式

```
=countif(E3:E812,">0")
```

* 總訂購量結算行程式

```
=sum(E3:E812)
```

