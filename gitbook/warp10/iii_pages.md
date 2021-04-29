## III. Visualize datas

Always in the Web Warp10 Studio, go to *Code* and select the Warp10 Backend Endpoint

![warp10_studio_conf3](imgs/warp10_studio_conf3.png "")

Then add and adapt the code below, with the correct token and channel

```
[ 'WARP10_READTOKEN' 
'sensor.data.DEMO'   <<< datas channel
{} NOW NOW ] 
FETCH 'gts' STORE $gts
```

Execute

![warp10_studio_datavize](imgs/warp10_studio_datavize.png "")

Then go to *Dataviz* and visualize datas

![warp10_studio_datavize2](imgs/warp10_studio_datavize2.png "")