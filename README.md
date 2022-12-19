# NCAA-Dashboard <br><br/>

### Dashboard
<p align="center">
<img width="650em" src="https://github.com/Power-BI-Solutions/NCAA-Dashboard/blob/main/NCAA%20Dashboard.gif" align = "center"/>
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

### Acknowledgement
Project is from WoW Power BI (Workout Wednesday)
- [Connect to data & create data model](https://www.youtube.com/watch?v=oiLuV0wBdTE&t=3s)
- [Create basic KPI report](https://www.youtube.com/watch?v=UTzOGBgPGMw&t=1s)
- [Report interactivity](https://www.youtube.com/watch?v=N8quTNUWuS0)
- [Set up dril through](https://www.youtube.com/watch?v=6aBH34BjEAA&list=PLz5da78rjfffsZ7RnN2QV__X6oXT36h1X&t=2s)


