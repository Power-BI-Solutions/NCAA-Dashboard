# NCAA-Dashboard <br><br/>

### Dashboard
<p align="center">
<img width="650em" src="" align = "center"/>
</p>
<br><br/>

### Data Source
- [NCAA Profit and Losses.xlxs](https://github.com/Power-BI-Solutions/NCAA-Dashboard/blob/main/NCAA%20Profit%20and%20Losses.xlsx)

Data required filtering as follows:

```dax
= Table.SelectRows(#"Promoted Headers", each ([NCAA Subdivision] = "Football Bowl Subdivision"))
```


```dax
= Table.SelectRows(#"Changed Type", each ([Total Expenses] <> null))
```

<br><br/>

### Custom Column
I used the following to create custom column:

```dax
= Table.AddColumn(#"Changed Type1", "Total Profits", each [Total Revenues]-[Total Expenses]+[Excess Transfers Back])
``` 

<br><br/>

### Model

<p align="center">
<img width="650em" src="https://github.com/Power-BI-Solutions/NCAA-Dashboard/blob/main/ncaa_data.png" align = "center"/>
</p>
<br><br/>

### 

