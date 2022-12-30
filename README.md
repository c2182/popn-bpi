## popn-radar

# 概要

ポップン レベル46 楽曲の実力をBPI計算式で数値化するスクリプトです。

<img src="https://user-images.githubusercontent.com/9925125/203383102-e3213231-4924-4e3a-8af9-6b723e8a5191.PNG" width="500">

下記の内容をとても参考にしています。  
・ポックラ一覧を出すスクリプト (作成者:まつまつ様)  
[https://github.com/ssdh233/popn-class](https://github.com/ssdh233/popn-class)  
・BPIとは (作成者:norimiso様)  
[http://norimiso.web.fc2.com/aboutBPI.html](http://norimiso.web.fc2.com/aboutBPI.html)  

# 使い方

1. 以下をブックマークに保存する。

```
javascript: void !function(e){var t=e.createElement("script");t.type="text/javascript",t.src="///cdn.jsdelivr.net/gh/c2182/popn-radar/dist/bundle.js",e.head.appendChild(t)}(document);
```

2. [ポップンのサイト](https://p.eagate.573.jp/game/popn/peace/p/playdata/index.html)にログインして、1で追加したブックマークをクリックする。

# BPIによる順位予測

| BPI | Rank(/1000) | Rank(/750) | Rank(/500) | 目安 |
|--|--|--|--|--|
| 100 | 1 | 1 | 1 | |
| 90 | 2 | 1.9 | 1.9 | KAC優勝 |
| 80 | 4 | 3.8 | 3.5 | |
| 70 | 7.9 | 7.3 | 6.5 | KAC決勝進出↑ |
| 60 | 15.8 | 14.1 | 12 | |
| 50 | 31.6 | 27.4 | 22.4 | ポックラ100.00↑ |
| 40 | 63.1 | 53.1 | 41.6 | |
| 30 | 125.9 | 102.9 | 77.5 | ポックラ99.50↑ |
| 20 | 251.2 | 199.5 | 144.3 | |
| 10 | 501.2 | 386.9 | 268.6 | |
| 0 | 1000 | 750 | 500 | ポックラ98.50～99.00 |

# BPI計算用データ

| 項目 | 説明 |
|--|--|
| 集計日 | 2022/10/14 |
| 対象楽曲 | UniLab稼働開始時のレベル46 全214曲 |
| 皆伝平均(=k) | ポックラ98.00～100.00のプレイヤー約70名の平均スコア(ポックラ平均99.09) |
| 歴代全一(=z) | TOPスコア |

# BPI計算式

IIDXの[BPI定義式](http://norimiso.web.fc2.com/aboutBPI.html)から次を変更しています。

■変更前  
単曲BPI = 100*(ln(S’)/ln(Z’))^1.5 (s>=k)  
単曲BPI = -100*(-ln(S’)/ln(Z’))^1.5 (s<k)  
単曲BPI下限 = -15

■変更後  
単曲BPI = 100*(ln(S’)/ln(Z’))^1.175 (s>=k)  
単曲BPI = -100*(-ln(S’)/ln(Z’))^1.175 (s<k)  
単曲BPI下限 = 0

# ノーツレーダーのスコア（おまけ）

テーマごとに単曲BPI上位10曲を合計しています。

| 名称 | パラメーター概要 |
|--|--|
| NOTES | 総ノーツ数の多さ |
| CHORD | 同時押しの難しさ |
| PEAK | ノーツ数の瞬間密度 |
| TRICKY | ズレ押し、ハネリズム、ロングポップ君、連打などの難しさ|
| KAIDAN | 階段譜面の難しさ |
| SOF-LAN | BPM変化の難しさ|

# データ一覧

| テーマ | 曲名 | 皆伝平均 | 歴代全一 |
|--|--|--|--|
|	PEAK	|	3 A.M. ディテクティブ・ゲーム	|	96188	|	99644	|
|	NOTES	|	532nm	|	96299	|	99834	|
|	TRICKY	|	ABSOLUTE	|	95856	|	99502	|
|	TRICKY	|	Afterimage d'automne	|	94468	|	99365	|
|	PEAK	|	Akash	|	96037	|	99670	|
|	NOTES	|	Alicy	|	95953	|	99737	|
|	TRICKY	|	Amabie	|	96755	|	99784	|
|	PEAK	|	Angelic Jelly	|	95587	|	99657	|
|	TRICKY	|	Arcanos	|	96434	|	99675	|
|	SOF-LAN	|	BabeL ～Next Story～	|	93755	|	99172	|
|	KAIDAN	|	beat it together	|	95387	|	99575	|
|	CHORD	|	BEEF	|	97655	|	99722	|
|	NOTES	|	Blind	|	96416	|	99752	|
|	NOTES	|	BLSTR	|	95660	|	99603	|
|	KAIDAN	|	Bolide	|	95584	|	99361	|
|	NOTES	|	brave!	|	96645	|	99942	|
|	CHORD	|	Butter-FLY	|	98142	|	99935	|
|	NOTES	|	CARNIVOROUS	|	96927	|	99765	|
|	KAIDAN	|	CARTOON☆RagHour	|	95602	|	99465	|
|	PEAK	|	Cassandra	|	93862	|	99450	|
|	SOF-LAN	|	Chaos:Q	|	89346	|	98854	|
|	TRICKY	|	Cloud 9	|	95678	|	99710	|
|	TRICKY	|	coffee break	|	94164	|	99337	|
|	KAIDAN	|	Colors	|	93917	|	99157	|
|	SOF-LAN	|	Come to Life	|	94902	|	99536	|
|	KAIDAN	|	Crumble Soul	|	97197	|	99772	|
|	CHORD	|	CURUS	|	98247	|	99909	|
|	CHORD	|	Daily Lunch Special	|	96712	|	99761	|
|	NOTES	|	De-a lungul vietii	|	95257	|	99592	|
|	CHORD	|	Deep Magenta	|	97082	|	99805	|
|	TRICKY	|	demolizione	|	95609	|	99692	|
|	NOTES	|	Denpasar	|	96079	|	99820	|
|	PEAK	|	Desire	|	96652	|	99803	|
|	NOTES	|	Dimension Gale	|	96499	|	99950	|
|	PEAK	|	Drizzly Venom	|	96945	|	99669	|
|	KAIDAN	|	EBONY & IVORY	|	95649	|	99794	|
|	TRICKY	|	Echoes	|	95607	|	99594	|
|	NOTES	|	Engraved Mark	|	95917	|	99830	|
|	NOTES	|	Ensamble Forecast 3/28	|	96525	|	99611	|
|	SOF-LAN	|	Fly far bounce	|	95767	|	99458	|
|	PEAK	|	GALAXY FOREST 11.6&12 	|	91880	|	99305	|
|	NOTES	|	GET WILD	|	97303	|	99764	|
|	CHORD	|	GO²TOS	|	98314	|	99887	|
|	CHORD	|	Gotta Get My Groove On	|	97796	|	99918	|
|	CHORD	|	Gradation	|	96622	|	99810	|
|	CHORD	|	Greening	|	96663	|	99718	|
|	NOTES	|	HADROS GALE	|	96392	|	99794	|
|	SOF-LAN	|	H@appy Fever Forever!!	|	94334	|	99597	|
|	KAIDAN	|	High Gravity	|	96887	|	99901	|
|	NOTES	|	HYENA	|	95494	|	99879	|
|	CHORD	|	IKKI! Explosion	|	96186	|	99773	|
|	KAIDAN	|	INHERITANCE of WILL	|	96543	|	99757	|
|	KAIDAN	|	Inside Insight	|	97182	|	99685	|
|	NOTES	|	Into The Light	|	97748	|	99842	|
|	KAIDAN	|	Kicky Kemari Kicker	|	96149	|	99902	|
|	SOF-LAN	|	Les Vague	|	95517	|	99660	|
|	PEAK	|	Linus	|	95639	|	99683	|
|	NOTES	|	Little Little Princess	|	97763	|	99822	|
|	NOTES	|	LOTUS	|	96716	|	99876	|
|	SOF-LAN	|	L'eternita	|	92877	|	98932	|
|	KAIDAN	|	MADSPEED狂信道	|	94626	|	98698	|
|	SOF-LAN	|	Magical 4	|	91958	|	99045	|
|	SOF-LAN	|	Miracle 4	|	94297	|	99526	|
|	KAIDAN	|	MOON	|	96144	|	99947	|
|	KAIDAN	|	nalca	|	96241	|	99769	|
|	CHORD	|	NEW PEOPLE	|	97283	|	99883	|
|	NOTES	|	On top of the world	|	95760	|	99473	|
|	PEAK	|	Over Da Moon	|	97009	|	99781	|
|	NOTES	|	Pacify	|	96639	|	99822	|
|	KAIDAN	|	paparazzi	|	96324	|	99584	|
|	CHORD	|	Phlox	|	97447	|	99669	|
|	SOF-LAN	|	Popperz Chronicle	|	90729	|	98433	|
|	CHORD	|	Poppin' Soda	|	98434	|	99907	|
|	NOTES	|	Psyche Planet-V	|	94981	|	99736	|
|	CHORD	|	pure	|	96499	|	99896	|
|	KAIDAN	|	Red Cape Theorem	|	96710	|	99724	|
|	PEAK	|	Riot of Color	|	95567	|	99840	|
|	SOF-LAN	|	say...but in vain	|	94379	|	99376	|
|	KAIDAN	|	Scarlet Pinheel	|	96361	|	99736	|
|	KAIDAN	|	\"Schall\" we step？	|	95523	|	99604	|
|	SOF-LAN	|	School Life	|	93837	|	99299	|
|	CHORD	|	SESSION With You!	|	97795	|	99809	|
|	PEAK	|	Shades of Day	|	96866	|	99702	|
|	NOTES	|	Shining Wizard	|	96563	|	99867	|
|	PEAK	|	SHION（VENUS mix）	|	96448	|	99618	|
|	KAIDAN	|	Six String Proof	|	95012	|	99355	|
|	KAIDAN	|	Soul On Fire	|	96493	|	99764	|
|	PEAK	|	SPEED KING ON FIRE	|	95827	|	99480	|
|	SOF-LAN	|	SPICY PIECE (Ryu☆Remix)	|	95332	|	99751	|
|	KAIDAN	|	Stella Sinistra	|	95129	|	99559	|
|	TRICKY	|	Strawberry Chu♡Chu♡	|	95490	|	99302	|
|	NOTES	|	Struggle	|	97393	|	99861	|
|	KAIDAN	|	SUPER SUMMER SALE	|	96835	|	99805	|
|	CHORD	|	Sweet,Sweet,Sweet.	|	97526	|	99854	|
|	KAIDAN	|	Symsonic Breeze	|	96052	|	99947	|
|	NOTES	|	Synergy For Angels	|	95267	|	99742	|
|	KAIDAN	|	The Sky of Sadness	|	96105	|	99592	|
|	NOTES	|	The Zoo Zone	|	95977	|	99911	|
|	NOTES	|	TOXIC VIBRATION	|	96008	|	99763	|
|	TRICKY	|	UNBOUND MIND	|	96849	|	99621	|
|	NOTES	|	Welcome to pop'n fantasy	|	97246	|	99946	|
|	PEAK	|	will	|	95751	|	99758	|
|	KAIDAN	|	Windy Fairy	|	96109	|	99571	|
|	NOTES	|	World Spider Web	|	96174	|	99762	|
|	NOTES	|	ZEPHYRANTHES	|	96351	|	99976	|
|	PEAK	|	μ9	|	96802	|	99883	|
|	NOTES	|	哀彩	|	97094	|	99857	|
|	KAIDAN	|	蒼い弓箭	|	96762	|	99814	|
|	PEAK	|	蒼が消えるとき	|	96488	|	99699	|
|	PEAK	|	緋月の狂想曲	|	95209	|	99548	|
|	PEAK	|	朱と碧のランページ	|	97541	|	99954	|
|	TRICKY	|	浅見文彦の事件簿～迷宮荘のワンピース	|	94840	|	98950	|
|	PEAK	|	明日への誓い	|	96458	|	99680	|
|	KAIDAN	|	アルストロメリア	|	96889	|	99815	|
|	CHORD	|	アルレシャ	|	97895	|	99973	|
|	CHORD	|	アンデスの太陽	|	97493	|	99793	|
|	NOTES	|	怒りと共に去りぬ！！	|	97214	|	99848	|
|	SOF-LAN	|	怒れる大きな白い馬～S.S.D.の役～	|	94362	|	99405	|
|	PEAK	|	一触即発☆禅ガール	|	94889	|	99521	|
|	NOTES	|	異能対決!VS.淀ジョル	|	96613	|	99953	|
|	TRICKY	|	ウソツキ横丁は雨模様	|	95155	|	99488	|
|	KAIDAN	|	憂恋☆アクティベーション	|	96314	|	99781	|
|	SOF-LAN	|	永遠という名の媚薬 ～Pyramid Power・Death Match ver.～	|	90429	|	99234	|
|	PEAK	|	おーまい！らぶりー！すうぃーてぃ！だーりん！	|	96028	|	99452	|
|	NOTES	|	おたすけ！アン子ちゃん (シノビアンレディーのテーマ 弐)	|	95852	|	99558	|
|	CHORD	|	カタルシスの月	|	97819	|	99924	|
|	SOF-LAN	|	ガッテンだ！！	|	93321	|	99510	|
|	PEAK	|	烏	|	96713	|	99946	|
|	PEAK	|	ギターケンドー	|	96677	|	99832	|
|	NOTES	|	キャトられ♥恋はモ～モク	|	95679	|	99615	|
|	NOTES	|	狂水一華	|	96835	|	99688	|
|	NOTES	|	キルト	|	97255	|	99909	|
|	TRICKY	|	禁じられた契約	|	97259	|	99848	|
|	CHORD	|	空想モダニズム	|	98285	|	99975	|
|	PEAK	|	空想モダニズム -Alice Schach remix-	|	96371	|	99426	|
|	NOTES	|	黒髪乱れし修羅となりて	|	95561	|	99934	|
|	NOTES	|	黒き螺旋のクレイドル	|	97230	|	99928	|
|	CHORD	|	結果オーライ！相性チェック	|	98502	|	99874	|
|	PEAK	|	玄兎ノ舞	|	96491	|	99925	|
|	KAIDAN	|	ゴールデンハート　ft. Kimberley Nutbey	|	97103	|	99801	|
|	NOTES	|	恋とメロンとキューピット	|	95305	|	99794	|
|	CHORD	|	恋はどう？モロ◎波動OK☆方程式！！	|	97166	|	99740	|
|	PEAK	|	黒点	|	95567	|	99409	|
|	KAIDAN	|	コルドバの女	|	96084	|	99683	|
|	TRICKY	|	コンビニエンスドラマ	|	95702	|	99518	|
|	CHORD	|	左脳スパーク	|	97297	|	99847	|
|	TRICKY	|	サヨナラ・ヘヴン	|	95862	|	99267	|
|	TRICKY	|	残酷な天使のテーゼ	|	96882	|	99896	|
|	SOF-LAN	|	幸せを謳う詩	|	95313	|	99732	|
|	CHORD	|	辞世テンプレート	|	96739	|	99690	|
|	KAIDAN	|	シャムシールの舞	|	96171	|	99796	|
|	NOTES	|	人妖絵巻其の二「鬼」～夜叉の祭は終夜～	|	96944	|	99810	|
|	CHORD	|	水月鏡花のコノテーション	|	98080	|	99953	|
|	NOTES	|	青春の扉	|	94281	|	99871	|
|	KAIDAN	|	零と弌の鍵の唄	|	95549	|	99653	|
|	KAIDAN	|	千年ノ理	|	96032	|	99756	|
|	TRICKY	|	そこはかとなくロマンセ	|	96130	|	99562	|
|	PEAK	|	√太陽系◎ドーナツ化計画∞∀∞	|	96644	|	99703	|
|	KAIDAN	|	魂依	|	96157	|	99652	|
|	PEAK	|	地方創生☆チクワクティクス	|	96228	|	99796	|
|	CHORD	|	超恋愛☆エクストリーム・ガール	|	97516	|	99816	|
|	KAIDAN	|	チルノのパーフェクトさんすう教室	|	96475	|	99714	|
|	PEAK	|	つばめ	|	95791	|	99819	|
|	PEAK	|	徹頭徹尾Thrive at Perfect Fourth	|	96256	|	99674	|
|	SOF-LAN	|	天上の星 ～黎明記～	|	96824	|	99810	|
|	CHORD	|	電波の暮らし	|	97570	|	99883	|
|	CHORD	|	桃花恋情	|	98143	|	99791	|
|	CHORD	|	どうなっちゃったって	|	95790	|	99867	|
|	TRICKY	|	鳥無き島にて	|	95496	|	99590	|
|	NOTES	|	取り残された美術(Arranged:HiZuMi)	|	97118	|	99812	|
|	CHORD	|	†渚の小悪魔ラヴリィ～レイディオ†	|	97127	|	99931	|
|	CHORD	|	ナスカの丘	|	97568	|	99672	|
|	KAIDAN	|	懐色坂	|	96198	|	99634	|
|	SOF-LAN	|	西麻布水道曲	|	88456	|	98388	|
|	KAIDAN	|	ネリと琥珀糖	|	96546	|	99766	|
|	NOTES	|	旗（Mystic Mix）	|	95715	|	99875	|
|	PEAK	|	洟・月・奇蹟	|	96220	|	99734	|
|	KAIDAN	|	疾風	|	96350	|	99743	|
|	NOTES	|	霽れと褻と穢れ	|	97443	|	99655	|
|	NOTES	|	表裏一体！？怪盗いいんちょの悩み♥	|	96171	|	99587	|
|	CHORD	|	プリンシプル	|	97816	|	99980	|
|	NOTES	|	ブルーローズイノセンス	|	96730	|	99817	|
|	NOTES	|	プロレタリア狂騒歌	|	96232	|	99732	|
|	KAIDAN	|	ペリーでぇす！	|	96412	|	99876	|
|	PEAK	|	鳳凰～Chinese Phoenix Mix～	|	93609	|	99234	|
|	KAIDAN	|	ぼくらの16bit戦争	|	96323	|	99558	|
|	KAIDAN	|	星屑の夜果て	|	96482	|	99669	|
|	KAIDAN	|	星屑ブレスレット	|	95847	|	99556	|
|	PEAK	|	ほしのつくりかた	|	97449	|	100000	|
|	CHORD	|	ボタン	|	97552	|	99794	|
|	KAIDAN	|	ポチコの幸せな日常	|	96412	|	99695	|
|	KAIDAN	|	ホピタスコピラ	|	95217	|	99719	|
|	NOTES	|	滅びに至るエランプシス	|	97387	|	99928	|
|	KAIDAN	|	マイアガル、マイオドル	|	96459	|	99804	|
|	KAIDAN	|	マインド・ゲーム	|	96422	|	99946	|
|	SOF-LAN	|	魔界！痛快！ヘルダンス	|	94696	|	99427	|
|	PEAK	|	巻寿司戦隊ウマイヤン ～コードネームはグリーン～	|	97546	|	99816	|
|	PEAK	|	曼珠沙華	|	96139	|	99901	|
|	SOF-LAN	|	乱れた風紀に天罰を	|	93843	|	99380	|
|	SOF-LAN	|	ミラクル・スイート・スイーツ・マジック！！	|	96814	|	99529	|
|	CHORD	|	無意識のフィロソフィア	|	96821	|	99670	|
|	CHORD	|	夢幻ノ光	|	98164	|	99892	|
|	CHORD	|	めうめうぺったんたん！！	|	96892	|	99764	|
|	CHORD	|	ラピストリアの約束	|	97950	|	99901	|
|	NOTES	|	ランカーキラーガール	|	97028	|	99809	|
|	KAIDAN	|	リナリア	|	96199	|	99637	|
|	PEAK	|	麗破唖甦～rebirth～	|	96508	|	99925	|
|	NOTES	|	流星☆ハニー Perforation Mix	|	95469	|	99782	|
|	CHORD	|	繚乱ヒットチャート	|	94694	|	99436	|
|	NOTES	|	凛として咲く花の如く	|	97362	|	99976	|
|	TRICKY	|	レトロスペクト路	|	96715	|	99602	|
|	NOTES	|	恋愛観測 -Rock Band Ver.-	|	96946	|	99850	|
|	NOTES	|	六兆年と一夜物語	|	96881	|	99796	|
|	CHORD	|	路男	|	96973	|	99832	|
