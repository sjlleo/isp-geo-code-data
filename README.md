# isp-geo-code-data
维护目前主流的 T1 ISP 骨干网所对应的三位码（IATA）地理位置信息

## 如何提交信息

右上角 fork 一份，将您的数据放入 IATA-ISP.csv 中，然后发起一个 pull request 请求即可。

---

注意1：为了方便规则匹配，注意提交的数据不要有**空格以及大小写，特别是城市由2个单词组成时**。

---

注意2：新增数据需要提供相应城市的 `rDNS` 以作为证明

如需要提交法兰克福、凤凰城的 `Cogentco` 数据，请在 pull request 中附上 `Cogentco` 在该城市的 `rDNS` 信息

以下是个例子

```
新增城市:
fra - 德国 黑森州 法兰克福 - cogentco
phx - 美国 亚利桑那州 凤凰城 - cogentco
nwrk - nj - 美国 特拉华州 纽瓦克 - ntt
tokyo - 日本 东京都 东京 - level3


rDNS: 
154.54.37.30 - be2846.rcr22.fra06.atlas.cogentco.com
154.54.42.65 - be2929.ccr31.phx01.atlas.cogentco.com
129.250.6.87 - ae-2.r00.nwrknj03.us.bb.gin.ntt.net
4.68.38.225 - ae-9.edge1.Tokyo4.Level3.net
```

## 额外信息
1. NTT 在马来西亚的地理信息

NTT 在马来西亚的PoP rDNS 是 : ```ae-8.r01.kslrml02.my.bb.gin.ntt.net```

其中的 ```kslrml``` 前四位是NTT代表 City/城市 的代码

根据 [NTT 官网](https://www.gin.ntt.net/support-center/policies-procedures/maintenance/) ```kslrml``` 属于 Kuala Lumpur (马来西亚吉隆坡联邦直辖区)

可是 ```kslr``` 是 Kuala Selangor (瓜拉雪兰莪) 的缩写 

Kuala Selangor (瓜拉雪兰莪) 是一个隶属于 Selangor (雪兰莪) 州里面的 District (县) , 并非隶属于 Kuala Lumpur (马来西亚吉隆坡联邦直辖区)

由于我们无法确定他真正地理位置实在 Kuala Selangor (瓜拉雪兰莪) 还是 Kuala Lumpur (马来西亚吉隆坡联邦直辖区) , 我们将两份数据整合在一起 , NTT 关于 ```kslrml``` 的 rDNS 都会被归类为 Kuala Lumpur / KUL (马来西亚吉隆坡联邦直辖区)

在 ```isp_city_4_ntt``` 和 ```province_code_4_ntt``` 一栏则会使用 ```kslr``` 和  ```ml``` 

因此```kslrml```将会被定义成 Kuala Lumpur / KUL (马来西亚吉隆坡联邦直辖区)


## 贡献者名单

[sjlleo (i@leo.moe)](https://github.com/sjlleo)

[isyekong (yekongtat@gmail.com)](https://github.com/isyekong)

[samleong123 (samsam123@samsam123.name.my)](https://github.com/samleong123)
