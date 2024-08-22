# ADS

[Smithsonian/NASA Astrophysics Data System (ADS)](https://ui.adsabs.harvard.edu) は、宇宙物理分野で非常によく使われる論文検索サイトで、効率的に研究を進める上で必須のサイトです。[arXiv](arxiv.md)のプレプリントといろいろな雑誌に出版された論文を両方検索できます。

## 使い方の例
* 著者名などで検索して、目的の論文を探すことができます。
* タイトルやアブストラクトでキーワードに引っかかる論文の一覧を出力して、面白そうな論文を手早く探すことができます。
* それぞれの論文に対し、arXivや出版された雑誌へと簡単に辿れるので、論文の中身をすばやくチェックできます。
* それぞれの論文に対し、`Refereces`からその論文中で引用している論文の一覧を、`Citations`からその論文を引用している論文の一覧をそれぞれ取得できるので、芋蔓式に関連論文を調べることができます。
* ある条件で引っかかった論文のリストに対して、例えば引用数でソートできます。
* 検索した論文に対して、`Export Citation`からLaTeXで使うbibtex形式など様々な形式で論文情報をアプトプットできます。

## より具体的な検索の例

Masamune Oguriを著者名に含む論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A%22Oguri%2C%20Masamune%22%20database%3Aastronomy&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
 author:"Oguri, Masamune" database:astronomy
 ```

Masamune Oguriを著者名に含む査読付き論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A%22Oguri%2C%20Masamune%22%20database%3Aastronomy%20property%3Arefereed&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
 ```
 author:"Oguri, Masamune" database:astronomy property:refereed 
```

Masamune Oguriが筆頭著者の査読付き論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A%22%5EOguri%2C%20Masamune%22%20property%3Arefereed%20database%3Aastronomy&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
author:"^Oguri, Masamune" property:refereed database:astronomy
```

Masamune Oguriが第二筆頭ないし第三筆頭著者の査読付き論文 ([link](https://ui.adsabs.harvard.edu/search/q=pos(author%3A%22Oguri%2C%20Masamune%22%2C%202%2C%203)%20property%3Arefereed%20database%3Aastronomy&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
pos(author:"Oguri, Masamune", 2, 3) property:refereed database:astronomy
```

Masamune Oguriを著者名に含む、2010年から2012年に出版された査読付き論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A%22Oguri%2C%20Masamune%22%20database%3Aastronomy%20property%3Arefereed%20year%3A2010-2012&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
author:"Oguri, Masamune" database:astronomy property:refereed year:2010-2012
```

Masamune Oguriを著者名に含む、2018年4月から2019年3月に出版された査読付き論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A%22Oguri%2C%20Masamune%22%20database%3Aastronomy%20property%3Arefereed%20pubdate%3A%5B2018-04%20TO%202019-03%5D%20&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
author:"Oguri, Masamune" database:astronomy property:refereed pubdate:[2018-04 TO 2019-03] 
```

Masamune OguriとRyuichi Takahashiを著者名に含む査読付き論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A(%22Oguri%2C%20Masamune%22%20%22Takahashi%2C%20Ryuichi%22)%20database%3Aastronomy%20property%3Arefereed%20&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
author:("Oguri, Masamune" "Takahashi, Ryuichi") database:astronomy property:refereed 
```

Masamune Oguriを著者名に含むNatureまたはScienceまたはNature Astronomyに出版された論文 ([link](https://ui.adsabs.harvard.edu/search/q=author%3A%22Oguri%2C%20Masamune%22%20bibstem%3A(Natur%20OR%20Sci%20OR%20NatAs)&sort=date%20desc%2C%20bibcode%20desc&p_=0))
```
author:"Oguri, Masamune" bibstem:(Natur OR Sci OR NatAs)
```

アブストラクトまたはタイトルにgravitational lensingを含む論文 ([link](https://ui.adsabs.harvard.edu/search/fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq_database=(database%3Aastronomy%20OR%20database%3Aphysics)&p_=0&q=%20abs%3A%22gravitational%20lensing%22&sort=date%20desc%2C%20bibcode%20desc&p_=0))
```
abs:"gravitational lensing"
```

本文中にlensed supernovaeを含む論文 ([link](https://ui.adsabs.harvard.edu/search/fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq_database=(database%3Aastronomy%20OR%20database%3Aphysics)&p_=0&q=full%3A%22lensed%20supernovae%22&sort=date%20desc%2C%20bibcode%20desc&p_=0))
```
full:"lensed supernovae"
```

謝辞に20H05856またはJP20H05856を含む論文 ([link](https://ui.adsabs.harvard.edu/search/q=ack%3A(20H05856%20OR%20JP20H05856)&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
ack:(20H05856 OR JP20H05856)
```

謝辞に20H05856またはJP20H05856を含む2022年4月から2023年3月に出版された論文 ([link](https://ui.adsabs.harvard.edu/search/q=ack%3A(20H05856%20OR%20JP20H05856)%20pubdate%3A%5B2022-04%20TO%202023-03%5D%20&sort=date%20desc%2C%20bibcode%20desc&p_=0)):
```
ack:(20H05856 OR JP20H05856) pubdate:[2022-04 TO 2023-03] 
```

## Export Citation

検索結果を探した後、`Export Citation`からbibtex形式など様々な形式で論文情報をアウトプットできます。論文等をLaTeXで執筆するときは、bibtexを使うにせよthebibliography環境を使うにせよ、引用論文リストは*決して手打ちせずに*ADSの検索結果をExportしてそれをコピペするようにしてください。

`Export Citation`で`Custom Format`を選ぶことで、アウトプット形式を自分で指定することができるので、これを習得することで複雑な状況にも対応できるようになります。詳細は[ADSの解説のページ](https://ui.adsabs.harvard.edu/help/actions/export)を参照してもらえば良いですが、以下参考のためいくつか具体例を示します。

DOIのみを出力:
```
%d
```

東京大学宇宙理論研究室（UTAP）で使われていた年次報告用の形式:
```
%ZEncoding:latex\\bibitem[utap_oguri_%zn] %g, %Y, %q, %V, %p %%%D
```

ダークマター学術変革のスプレッドシート用:
```
%o\t%T\t%q, %V, %p\t%Y\t%d\n
```

[一覧に戻る](README.md)

