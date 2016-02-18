## 使用div制作表格时，div之间的空格问题

当使用div+css的方式来制作一个表格时，为了将多个div放在同一行，会将div的dispaly设为inline-block这个时候 如果div之间换行或者有空格那么显示的时候就会有空隙，解决的办法很简单可以将div放在同一行或者margin的值设为负



```javascript
因为div之间换行而且设为inlin-block所以会出现空隙
 <div class="bill-user-info">
 <div class="bill-inline-block">名称：</div>
 <div class="bill-inline-block">杭州税友集团</div></div>
 <div class="bill-user-info"><div class="bill-inline-block">纳税人识别号：</div><div class="bill-inline-block">000000000</div>
 </div>
<div class="bill-user-info"><div class="bill-inline-block">地址，电话：</div><div class="bill-inline-block">0571-00000000</div></div>
设置margin值来消除空隙
.bill-inline-block{
    display: inline-block;
    vertical-align: top;
    margin-right: -4px;
}
```