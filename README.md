## popn-bpi

# 概要

Lv46,47,48 の実力をBPI風に数値化するツールです。

<img src="https://user-images.githubusercontent.com/9925125/210038837-38867676-a9c7-445f-83db-97077ae6abb2.PNG" width="500">

# 使い方

1. 以下をURLに指定して、ブックマークに保存する。

Lv46版
```
javascript: void !function(e){var t=e.createElement("script");t.type="text/javascript",t.src="///cdn.jsdelivr.net/gh/c2182/popn-bpi/dist/bpi46.js",e.head.appendChild(t)}(document);
```
Lv47版
```
javascript: void !function(e){var t=e.createElement("script");t.type="text/javascript",t.src="///cdn.jsdelivr.net/gh/c2182/popn-bpi/dist/bpi47.js",e.head.appendChild(t)}(document);
```
Lv48版
```
javascript: void !function(e){var t=e.createElement("script");t.type="text/javascript",t.src="///cdn.jsdelivr.net/gh/c2182/popn-bpi/dist/bpi48.js",e.head.appendChild(t)}(document);
```

2. [ポップンのサイト](https://p.eagate.573.jp/game/popn/peace/p/playdata/index.html)にログインして、1で追加したブックマークをクリックする。

# BPIによる順位予測

| BPI | Rank | 目安 |
|--|--|--|
| 100 | 1 | |
| 90 | 2 | KAC優勝 |
| 80 | 4 | |
| 70 | 7.9 | KAC予選通過 |
| 60 | 15.8 |  |
| 50 | 31.6 | |
| 40 | 63.1 | ポックラ100.00前後 |
| 30 | 125.9 | |
| 20 | 251.2 | ポックラ99.50前後 |
| 10 | 501.2 | |
| 0 | 1000 | ポックラ99.00前後 |

# BPI計算用データ

| 項目 | 説明 |
|--|--|
| 集計日 | 2022/12/30 |
| 対象楽曲 | 集計日時点の収録曲(Lv46:222曲,Lv47:198曲,Lv48:131曲)のうち 焱影(EX),Double Dribble(EX)の2曲以外|
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

# データ一覧

|  曲名 | 皆伝平均 | 歴代全一 |
|--|--|--|
|	001 -どうしんのかいろ-	|	95452	|	99397	|
|	3 A.M. ディテクティブ・ゲーム	|	96447	|	99644	|
|	532nm	|	96379	|	99834	|
|	ABSOLUTE	|	95887	|	99502	|
|	Afterimage d'automne	|	94524	|	99365	|
|	Akash	|	96069	|	99670	|
|	Alicy	|	95974	|	99737	|
|	Amabie	|	96763	|	99784	|
|	Angelic Jelly	|	95643	|	99657	|
|	Arcanos	|	96450	|	99675	|
|	BabeL ～Next Story～	|	93846	|	99172	|
|	beat it together	|	95464	|	99575	|
|	BEEF	|	97782	|	99722	|
|	Blind	|	96429	|	99752	|
|	BLSTR	|	95863	|	99603	|
|	Bolide	|	95611	|	99361	|
|	brave!	|	96753	|	99942	|
|	Butter-FLY	|	98131	|	99935	|
|	CARNIVOROUS	|	97050	|	99765	|
|	CARTOON☆RagHour	|	95597	|	99465	|
|	Cassandra	|	93888	|	99450	|
|	Chaos:Q	|	89410	|	98854	|
|	Cloud 9	|	95685	|	99710	|
|	coffee break	|	94194	|	99337	|
|	Colors	|	94305	|	99157	|
|	Come to Life	|	94902	|	99536	|
|	Crumble Soul	|	97247	|	99772	|
|	CURUS	|	98274	|	99909	|
|	Daily Lunch Special	|	96720	|	99761	|
|	De-a lungul vietii	|	95327	|	99592	|
|	Deep Magenta	|	97085	|	99805	|
|	demolizione	|	95611	|	99692	|
|	Denpasar	|	96264	|	99820	|
|	Desire	|	96692	|	99803	|
|	Dimension Gale	|	96507	|	99950	|
|	Drizzly Venom	|	96997	|	99669	|
|	EBONY & IVORY	|	95663	|	99794	|
|	Echoes	|	95621	|	99594	|
|	Engraved Mark	|	95922	|	99830	|
|	Ensamble Forecast 3/28	|	96576	|	99611	|
|	Fly far bounce	|	95801	|	99458	|
|	GALAXY FOREST 11.6&12 	|	91944	|	99305	|
|	GET WILD	|	97323	|	99764	|
|	GO²TOS	|	98356	|	99887	|
|	Gotta Get My Groove On	|	97798	|	99918	|
|	Gradation	|	96723	|	99810	|
|	Greening	|	96687	|	99718	|
|	HADROS GALE	|	96395	|	99794	|
|	HAGURUMA	|	96265	|	99363	|
|	H@appy Fever Forever!!	|	94252	|	99597	|
|	High Gravity	|	96962	|	99901	|
|	HYENA	|	95527	|	99879	|
|	IKKI! Explosion	|	96207	|	99773	|
|	INHERITANCE of WILL	|	96611	|	99757	|
|	Inside Insight	|	97191	|	99685	|
|	Into The Light	|	97759	|	99842	|
|	Kicky Kemari Kicker	|	96175	|	99902	|
|	Les Vague	|	95542	|	99660	|
|	Linus	|	95623	|	99683	|
|	Little Little Princess	|	97846	|	99822	|
|	LOTUS	|	96753	|	99876	|
|	L'eternita	|	92911	|	98932	|
|	MADSPEED狂信道	|	94626	|	98698	|
|	Magical 4	|	91960	|	99045	|
|	MA・TSU・RI	|	97285	|	99790	|
|	Miracle 4	|	94297	|	99526	|
|	MOON	|	96177	|	99947	|
|	nalca	|	96277	|	99769	|
|	NEW PEOPLE	|	97382	|	99883	|
|	On top of the world	|	95783	|	99473	|
|	Over Da Moon	|	97082	|	99781	|
|	Pacify	|	96691	|	99822	|
|	paparazzi	|	96422	|	99584	|
|	Phlox	|	97522	|	99713	|
|	Popperz Chronicle	|	90729	|	98433	|
|	Poppin' Soda	|	98445	|	99907	|
|	Psyche Planet-V	|	94992	|	99736	|
|	pure	|	96508	|	99896	|
|	Red Cape Theorem	|	96824	|	99724	|
|	Riot of Color	|	95593	|	99840	|
|	say...but in vain	|	94649	|	99376	|
|	Scarlet Pinheel	|	96424	|	99736	|
|	\"Schall\" we step？	|	95556	|	99604	|
|	School Life	|	93872	|	99299	|
|	SESSION With You!	|	97931	|	99809	|
|	Shades of Day	|	96935	|	99702	|
|	Shining Wizard	|	96602	|	99867	|
|	SHION（VENUS mix）	|	96468	|	99618	|
|	Six String Proof	|	95033	|	99355	|
|	Soul On Fire	|	96516	|	99764	|
|	SPEED KING ON FIRE	|	95854	|	99480	|
|	SPICY PIECE (Ryu☆Remix)	|	95394	|	99751	|
|	Stella Sinistra	|	95161	|	99559	|
|	Strawberry Chu♡Chu♡	|	95519	|	99327	|
|	Struggle	|	97407	|	99861	|
|	SUPER SUMMER SALE	|	96885	|	99805	|
|	Sweet,Sweet,Sweet.	|	97540	|	99854	|
|	Symsonic Breeze	|	96126	|	99947	|
|	Synergy For Angels	|	95454	|	99742	|
|	The Sky of Sadness	|	96215	|	99592	|
|	The Zoo Zone	|	95977	|	99911	|
|	TOXIC VIBRATION	|	96008	|	99763	|
|	UNBOUND MIND	|	96857	|	99621	|
|	Welcome to pop'n fantasy	|	97321	|	99946	|
|	will	|	95807	|	99758	|
|	Windy Fairy	|	96126	|	99571	|
|	World Spider Web	|	96279	|	99762	|
|	ZEPHYRANTHES	|	96449	|	99976	|
|	μ9	|	96845	|	99883	|
|	哀彩	|	97103	|	99857	|
|	蒼い弓箭	|	96745	|	99814	|
|	蒼が消えるとき	|	96523	|	99699	|
|	緋月の狂想曲	|	95341	|	99548	|
|	朱と碧のランページ	|	97611	|	99954	|
|	浅見文彦の事件簿～迷宮荘のワンピース	|	94914	|	98950	|
|	明日への誓い	|	96549	|	99680	|
|	アルストロメリア	|	96939	|	99815	|
|	アルレシャ	|	97914	|	99973	|
|	アンデスの太陽	|	97510	|	99793	|
|	怒りと共に去りぬ！！	|	97325	|	99848	|
|	怒れる大きな白い馬～S.S.D.の役～	|	94447	|	99405	|
|	一触即発☆禅ガール	|	94914	|	99521	|
|	異能対決!VS.淀ジョル	|	96711	|	99953	|
|	ウソツキ横丁は雨模様	|	95180	|	99488	|
|	憂恋☆アクティベーション	|	96364	|	99781	|
|	永遠という名の媚薬 ～Pyramid Power・Death Match ver.～	|	90505	|	99234	|
|	おーまい！らぶりー！すうぃーてぃ！だーりん！	|	96068	|	99452	|
|	おたすけ！アン子ちゃん (シノビアンレディーのテーマ 弐)	|	95897	|	99558	|
|	カタルシスの月	|	97873	|	99924	|
|	ガッテンだ！！	|	93358	|	99510	|
|	烏	|	96735	|	99946	|
|	ギターケンドー	|	96680	|	99832	|
|	キャトられ♥恋はモ～モク	|	95775	|	99615	|
|	狂水一華	|	96958	|	99688	|
|	キルト	|	97287	|	99909	|
|	禁じられた契約	|	97271	|	99848	|
|	空想モダニズム	|	98416	|	99975	|
|	空想モダニズム -Alice Schach remix-	|	96424	|	99478	|
|	黒髪乱れし修羅となりて	|	95597	|	99934	|
|	黒き螺旋のクレイドル	|	97236	|	99928	|
|	結果オーライ！相性チェック	|	98502	|	99874	|
|	玄兎ノ舞	|	96565	|	99925	|
|	ゴールデンハート　ft. Kimberley Nutbey	|	97140	|	99801	|
|	恋とメロンとキューピット	|	95439	|	99794	|
|	恋はどう？モロ◎波動OK☆方程式！！	|	97203	|	99740	|
|	黒点	|	95585	|	99409	|
|	コルドバの女	|	96084	|	99683	|
|	コンビニエンスドラマ	|	95736	|	99518	|
|	左脳スパーク	|	97450	|	99847	|
|	サヨナラ・ヘヴン	|	95915	|	99267	|
|	残酷な天使のテーゼ	|	96922	|	99896	|
|	幸せを謳う詩	|	95313	|	99732	|
|	辞世テンプレート	|	96740	|	99690	|
|	シャムシールの舞	|	96187	|	99796	|
|	人妖絵巻其の二「鬼」～夜叉の祭は終夜～	|	96968	|	99810	|
|	水月鏡花のコノテーション	|	98109	|	99953	|
|	青春の扉	|	94320	|	99871	|
|	零と弌の鍵の唄	|	95549	|	99653	|
|	千年ノ理	|	96044	|	99756	|
|	蒼氷のフラグメント	|	96139	|	99538	|
|	そこはかとなくロマンセ	|	96173	|	99562	|
|	√太陽系◎ドーナツ化計画∞∀∞	|	96664	|	99703	|
|	魂依	|	96167	|	99652	|
|	地方創生☆チクワクティクス	|	96351	|	99796	|
|	超恋愛☆エクストリーム・ガール	|	97629	|	99816	|
|	チルノのパーフェクトさんすう教室	|	96482	|	99714	|
|	つばめ	|	95909	|	99819	|
|	徹頭徹尾Thrive at Perfect Fourth	|	96303	|	99674	|
|	天上の星 ～黎明記～	|	96868	|	99810	|
|	電波の暮らし	|	97587	|	99883	|
|	桃花恋情	|	98156	|	99791	|
|	どうなっちゃったって	|	95803	|	99867	|
|	鳥無き島にて	|	95705	|	99590	|
|	取り残された美術(Arranged:HiZuMi)	|	97299	|	99812	|
|	†渚の小悪魔ラヴリィ～レイディオ†	|	97246	|	99931	|
|	ナスカの丘	|	97512	|	99672	|
|	懐色坂	|	96240	|	99634	|
|	西麻布水道曲	|	88817	|	98388	|
|	ネリと琥珀糖	|	96701	|	99766	|
|	ノープラン・デイズ	|	97497	|	99781	|
|	旗（Mystic Mix）	|	95722	|	99875	|
|	洟・月・奇蹟	|	96233	|	99734	|
|	疾風	|	96390	|	99743	|
|	霽れと褻と穢れ	|	97480	|	99655	|
|	表裏一体！？怪盗いいんちょの悩み♥	|	96195	|	99587	|
|	プリンシプル	|	97824	|	99980	|
|	ブルーローズイノセンス	|	96839	|	99817	|
|	プロレタリア狂騒歌	|	96331	|	99732	|
|	ペリーでぇす！	|	96470	|	99876	|
|	鳳凰～Chinese Phoenix Mix～	|	93643	|	99234	|
|	ぼくらの16bit戦争	|	96383	|	99558	|
|	星屑の夜果て	|	96486	|	99669	|
|	星屑ブレスレット	|	95965	|	99556	|
|	ほしのつくりかた	|	97471	|	100000	|
|	ボタン	|	97688	|	99794	|
|	ポチコの幸せな日常	|	96433	|	99695	|
|	ホピタスコピラ	|	95305	|	99719	|
|	ホムンクルスレシピ	|	97009	|	99687	|
|	滅びに至るエランプシス	|	97546	|	99928	|
|	マイアガル、マイオドル	|	96476	|	99804	|
|	マインド・ゲーム	|	96441	|	99946	|
|	魔界！痛快！ヘルダンス	|	94703	|	99427	|
|	巻寿司戦隊ウマイヤン ～コードネームはグリーン～	|	97562	|	99816	|
|	曼珠沙華	|	96158	|	99901	|
|	乱れた風紀に天罰を	|	93843	|	99380	|
|	ミラクル・スイート・スイーツ・マジック！！	|	96983	|	99529	|
|	無意識のフィロソフィア	|	96852	|	99670	|
|	夢幻ノ光	|	98178	|	99892	|
|	斑咲花	|	94814	|	99359	|
|	めうめうぺったんたん！！	|	97010	|	99764	|
|	ラピストリアの約束	|	97977	|	99901	|
|	ラブケミ	|	97116	|	99575	|
|	ランカーキラーガール	|	97001	|	99809	|
|	リナリア	|	96291	|	99637	|
|	麗破唖甦～rebirth～	|	96525	|	99925	|
|	流星☆ハニー Perforation Mix	|	95510	|	99782	|
|	繚乱ヒットチャート	|	94694	|	99436	|
|	凛として咲く花の如く	|	97392	|	99976	|
|	レトロスペクト路	|	96743	|	99602	|
|	恋愛観測 -Rock Band Ver.-	|	97005	|	99850	|
|	六兆年と一夜物語	|	96864	|	99796	|
|	路男	|	97004	|	99832	|
|	1/6billionth	|	96340	|	99773	|
|	50th Memorial Songs -The BEMANI History-	|	94160	|	99382	|
|	8000000	|	96422	|	99883	|
|	ACCELERATION	|	96219	|	99798	|
|	Aftermath	|	96938	|	99589	|
|	Amalgamation	|	95957	|	99703	|
|	Ancient Heritage	|	94755	|	99777	|
|	AsiaN distractive	|	96337	|	99511	|
|	ATTRACTION！	|	95039	|	99663	|
|	BBLLAASSTT!!	|	95548	|	99805	|
|	BEYOND THE EARTH	|	95558	|	99320	|
|	BILLION MONEY BAZOOKA	|	95206	|	99718	|
|	BLAZE∞BREEZE	|	96511	|	99787	|
|	Bye Bye	|	95773	|	99558	|
|	Caradbolg	|	96250	|	99402	|
|	Catch Our Fire!	|	96039	|	99793	|
|	Celsus	|	96860	|	99679	|
|	chilblain	|	96605	|	99807	|
|	Cleopatrysm	|	94885	|	99488	|
|	Craze for You	|	93536	|	99212	|
|	Dance to Blue (Respect Style)	|	94981	|	99631	|
|	Danza Pantera	|	97190	|	99578	|
|	Der Wald(kors k Remix)	|	95531	|	99748	|
|	DOES NOT COMPUTE	|	97361	|	99860	|
|	Dogu Ditty	|	95673	|	99776	|
|	El venenciador	|	94833	|	99579	|
|	Empty Backdoor	|	96902	|	99802	|
|	Fate No.23	|	95303	|	99744	|
|	Floccinaucinihilipilification	|	95505	|	99730	|
|	FLOWER	|	95042	|	99842	|
|	For Dear ～	|	97867	|	99884	|
|	full-consciousness green	|	95989	|	99890	|
|	Ge-Ko-Ku-Jo	|	96185	|	99769	|
|	Habits	|	95924	|	99509	|
|	Hatcha Metcha Party	|	96031	|	99590	|
|	Holy Forest	|	95926	|	99572	|
|	HypArcSin(x)	|	94838	|	99270	|
|	I just hate you	|	95863	|	99690	|
|	ice crystals	|	95503	|	99627	|
|	IMPLANTATION	|	93968	|	99835	|
|	In The Ruins	|	95821	|	99705	|
|	INFINITY	|	96672	|	99814	|
|	Invisible Farewell	|	93209	|	99338	|
|	I'm so Happy	|	96784	|	99905	|
|	Jack in the Box	|	95995	|	99560	|
|	Jetcoaster Windy	|	96591	|	99673	|
|	Journey	|	95172	|	99703	|
|	KIMONO♥PRINCESS	|	95299	|	99751	|
|	KING of the SEA	|	95080	|	99515	|
|	La Lumiere	|	94929	|	99604	|
|	LIKE A VAMPIRE	|	96080	|	99732	|
|	LIMIT TOPPA REVOLUTION	|	95115	|	99448	|
|	Little prayer	|	96594	|	99791	|
|	♥LOVE² シュガ→♥ (かめりあ&ななひら's Over-Sweet-Dempa ♥LOVE² シュガ→♥な恋愛教室 Remix)	|	94891	|	99626	|
|	Manhattan Sports Club	|	95242	|	99522	|
|	Maritare!	|	92463	|	99469	|
|	Miracle 4 RELOADED	|	91525	|	99219	|
|	Monkshood	|	94419	|	99382	|
|	murmur twins	|	94254	|	99682	|
|	Mychronicle	|	96143	|	99778	|
|	Mynarco	|	95435	|	99663	|
|	NINE PIECE	|	94948	|	99516	|
|	nostos	|	94056	|	99167	|
|	Nove Primavere	|	93543	|	99270	|
|	On dish or maindish?	|	97038	|	99692	|
|	ON-DO	|	95368	|	99664	|
|	Pa la la 42	|	94305	|	99361	|
|	Peragro	|	96236	|	99763	|
|	perditus†paradisus	|	93373	|	99083	|
|	PITAゴラス☆KISS	|	94820	|	99556	|
|	popcorn parade	|	95456	|	99530	|
|	PRANA	|	96501	|	99807	|
|	Princess Roki	|	96308	|	99485	|
|	PUNISHER	|	96130	|	99771	|
|	quaver♪	|	96514	|	99889	|
|	Reconsideration	|	95640	|	99625	|
|	Revived After Ruined Shine	|	96215	|	99346	|
|	Romance	|	97044	|	99823	|
|	Russian Caravan Rhapsody	|	95900	|	99730	|
|	SDVX REMIX SELECTION for pop'n music vol.01	|	94960	|	99462	|
|	Slime Molds	|	96335	|	99521	|
|	smile	|	96159	|	99727	|
|	SPACE CRASH LANDING	|	96531	|	99762	|
|	Spiral Clouds	|	94515	|	99151	|
|	Squeeze	|	95133	|	99737	|
|	STERLING SILVER	|	95832	|	99718	|
|	Stories	|	95355	|	99610	|
|	Sweet Sweet ♥ Magic	|	95355	|	99796	|
|	Swinging Skulls	|	95542	|	99377	|
|	The last of world music	|	95163	|	99403	|
|	THE SAFARI - NEETs ver. -	|	96837	|	99758	|
|	The tyro's reverie	|	92046	|	99311	|
|	TRUTH behind U	|	96833	|	99733	|
|	V	|	95598	|	99814	|
|	Versa	|	94233	|	99561	|
|	Violently Car	|	92664	|	99225	|
|	virkatoの主題によるperson09風超絶技巧変奏曲	|	93035	|	98049	|
|	virtual killer	|	94796	|	99488	|
|	Visterhv	|	96377	|	99743	|
|	Votum stellarum -forest #25 RMX-	|	94665	|	99358	|
|	αρχη	|	96222	|	99561	|
|	暴レ焔	|	95660	|	99615	|
|	在るが儘に	|	96591	|	99979	|
|	己経忍不住了	|	96193	|	99639	|
|	怒れる大きな白い馬	|	94220	|	99460	|
|	一発逆転！××だらけのハッピー大運動会！！	|	96350	|	99826	|
|	ヴェルヴェット　バレット	|	95463	|	99826	|
|	うた	|	95317	|	99328	|
|	永遠という名の媚薬	|	90782	|	97857	|
|	エイプリルフールの唄	|	97424	|	99713	|
|	エキサイティング！！も・ちゃ・ちゃ☆	|	95505	|	99784	|
|	焔華	|	96086	|	99566	|
|	お江戸花吹雪 TEYAN-day MIX	|	95645	|	99802	|
|	お米の美味しい炊き方、そしてお米を食べることによるその効果。	|	95709	|	99630	|
|	乙女繚乱 舞い咲き誇れ	|	97998	|	99930	|
|	踊るフィーバーロボ　Eu-Robot mix	|	95705	|	99801	|
|	朧月覆う雲をも裂きぬ	|	95442	|	99559	|
|	革命パッショネイト	|	97941	|	99843	|
|	カゲロウ	|	96473	|	99740	|
|	カタルシスの月	|	97550	|	99921	|
|	彼女は快刀乱麻	|	96947	|	99910	|
|	鴉	|	97767	|	99855	|
|	煌-灼熱の裁き-	|	96887	|	99827	|
|	キルト（Patchworker RMX）	|	96064	|	99627	|
|	クラゲータ	|	94786	|	99765	|
|	黒髪乱れし修羅となりて～凛 edition～	|	95131	|	99856	|
|	月光蝶	|	95323	|	99794	|
|	けもののおうじゃ★めうめう	|	96557	|	99863	|
|	元禄花吹雪	|	94639	|	99015	|
|	恋する☆宇宙戦争っ！！	|	95669	|	99448	|
|	乞い祈みの撫子	|	95964	|	99647	|
|	極悪の華	|	97073	|	99693	|
|	この子の七つのお祝いに	|	95217	|	99751	|
|	コルトーン	|	94006	|	99295	|
|	サケビノミドリ	|	96528	|	99520	|
|	差無来！！	|	94355	|	99350	|
|	猿の経	|	94935	|	99381	|
|	ジオメトリック∮ティーパーティー	|	94243	|	98897	|
|	十界	|	96918	|	99717	|
|	漆黒のスペシャルプリンセスサンデー	|	96969	|	99824	|
|	銃弾は解を撃ち抜いて	|	96650	|	99886	|
|	情操ディストピア	|	97118	|	99763	|
|	少年リップルズ	|	96124	|	99580	|
|	如雨露姫が世界征服	|	96486	|	99755	|
|	神曲	|	96154	|	99721	|
|	真超深ＴＩＯＮ	|	96487	|	99687	|
|	スーパーモグー	|	94645	|	99428	|
|	水晶塔のオルカ	|	94954	|	99215	|
|	ススメ！少年！！	|	95233	|	99770	|
|	ストレイ・マーチ	|	96190	|	99838	|
|	世界の果てに約束の凱歌を-pop'n ver.-	|	96569	|	99807	|
|	セツナトリップ	|	96607	|	99775	|
|	造花の貌	|	96500	|	99638	|
|	誰がために陽はのぼる	|	96094	|	99836	|
|	たまゆら	|	96532	|	99776	|
|	断罪プラズマ	|	95864	|	99595	|
|	男々道	|	89683	|	99258	|
|	ちくわパフェだよ☆ＣＫＰ	|	96652	|	99858	|
|	地の記　獄編	|	96504	|	99874	|
|	デパ地下のお話	|	96484	|	99820	|
|	デュスノミア	|	95425	|	99760	|
|	でんがなマンガナ	|	95578	|	99716	|
|	天空ジオグラフィ	|	94996	|	99464	|
|	天庭	|	96692	|	99914	|
|	天庭 おとこのこ編	|	96506	|	99606	|
|	天和無双	|	93192	|	99281	|
|	突然ゴルゴンゾーラ	|	96210	|	99745	|
|	嘆きの樹 (BEMANI SYMPHONY Arr.)	|	91885	|	99232	|
|	なまいきプリンセス	|	96463	|	99595	|
|	猫侍の逆襲	|	94165	|	99270	|
|	螺子之人	|	92591	|	99420	|
|	背水之陣	|	94696	|	99549	|
|	ハラショー！おにぎりサーカス団☆	|	95143	|	99669	|
|	薔薇は永遠に美しく	|	95287	|	99329	|
|	叛逆のディスパレート	|	96798	|	99775	|
|	バンブーソード・ガール	|	94420	|	99383	|
|	白夜幻燈	|	95072	|	99280	|
|	フリーパス	|	95161	|	99434	|
|	文明開化	|	95864	|	99752	|
|	へんたいトリロジー	|	97883	|	99935	|
|	ホーンテッド★メイドランチ	|	96503	|	99839	|
|	鳳凰～Chinese Phoenix Mix～	|	93890	|	99374	|
|	放課後コンチェルティーノ～私だけの部室狂騒曲	|	93521	|	99326	|
|	ほおずき程度には赤い頭髪	|	94596	|	99405	|
|	僕らの旅はどこまでも	|	89308	|	98865	|
|	ポルターガイスト	|	94734	|	99378	|
|	ませまてぃっく♥ま+ま=まじっく！	|	96551	|	99933	|
|	ミサコの日記（見ちゃダメ！）	|	95200	|	99679	|
|	ムーニャポヨポヨスッポコニャーゴ	|	95102	|	99774	|
|	明鏡止水	|	94959	|	99361	|
|	メンテナンス物語	|	96692	|	99729	|
|	もうあおむけでいくしかない	|	95054	|	99397	|
|	ユメブキ	|	96954	|	99853	|
|	雷君	|	96165	|	99857	|
|	六花美人	|	95111	|	99642	|
|	龍と少女とデコヒーレンス	|	95090	|	99819	|
|	凛として咲く花の如く　～ひなビタ♪edition～	|	96960	|	99935	|
|	黎明スケッチブック	|	95068	|	99360	|
|	Aithon	|	95406	|	99474	|
|	Alia Dimensiva	|	92221	|	99023	|
|	ANNIVERSARY ∴∵∴ ←↓↑→	|	94469	|	99495	|
|	asteer	|	94584	|	99227	|
|	BabeL ～Grand Story～	|	95321	|	99446	|
|	Battle Against a True Hero/本物のヒーローとの戦い	|	95233	|	99600	|
|	Celsus Ⅱ	|	96773	|	99841	|
|	CHIP'N'RIDDIM	|	93818	|	99666	|
|	Chronoxia	|	94487	|	99742	|
|	Concertare	|	92794	|	99681	|
|	Concertino In Blue	|	94161	|	99378	|
|	cucumis melo	|	92416	|	99520	|
|	DDR MEGAMIX	|	88883	|	99145	|
|	Dimensiva Vulnus	|	94242	|	99474	|
|	Doll's sight	|	91306	|	99436	|
|	Dracophobia	|	92694	|	98878	|
|	DUAL STRIKER	|	95369	|	99591	|
|	Ergosphere	|	95470	|	99410	|
|	Esperanza	|	94254	|	99170	|
|	Evans	|	94475	|	99708	|
|	fffff	|	93288	|	99418	|
|	fffff op.2	|	92639	|	98591	|
|	FLOWER	|	94199	|	99662	|
|	forever under construction	|	94479	|	99584	|
|	Funky sonic World	|	94905	|	99727	|
|	GAIA	|	93088	|	99298	|
|	Globe Glitter	|	94010	|	99250	|
|	GOLDEN CROSS	|	94606	|	99848	|
|	good night , mommy	|	94871	|	99676	|
|	Grand Chariot	|	94033	|	99563	|
|	Gray clouds	|	94673	|	99679	|
|	hora de verdad	|	92456	|	98686	|
|	Idola	|	95614	|	99856	|
|	Indigo Nocturne	|	95138	|	99584	|
|	JOMANDA	|	92434	|	99306	|
|	KETER	|	95332	|	99455	|
|	La fame di Adria	|	94399	|	99123	|
|	LEAD Gravity（M）	|	94489	|	99411	|
|	Leaf	|	93407	|	99467	|
|	Life is beautiful	|	92628	|	99135	|
|	Little prayer	|	94062	|	99686	|
|	Macuilxochitl	|	94230	|	99560	|
|	MADSPEED狂信道	|	93192	|	99207	|
|	Majestaria	|	95431	|	99665	|
|	MEGALOVANIA	|	95228	|	99466	|
|	Metamorphose	|	94348	|	99511	|
|	Mirage Age	|	95126	|	99636	|
|	MVA	|	93507	|	99366	|
|	NOBUNAGA	|	95316	|	99834	|
|	Northern Cross	|	94373	|	99604	|
|	nostos	|	92377	|	98835	|
|	OVERHEAT -Type P-	|	93045	|	99282	|
|	POP-STEP-UP	|	88689	|	99226	|
|	Puberty Dysthymia	|	93958	|	99291	|
|	Raison d'être～交差する宿命～	|	93884	|	99390	|
|	Red Roses	|	94501	|	99710	|
|	Russian Caravan Rhapsody	|	94657	|	99485	|
|	Sanctum Crusade	|	94239	|	99239	|
|	saQrifice	|	94216	|	99576	|
|	Southern Cross	|	94601	|	99656	|
|	STULTI	|	92333	|	99231	|
|	SYMPHONY FROM ZERO	|	93725	|	99545	|
|	The Least 100 sec	|	95881	|	99608	|
|	Trill auf G	|	93685	|	99287	|
|	Trixxxter	|	93805	|	99523	|
|	True Blue	|	95919	|	99786	|
|	ULTRA BUTTERFLY(坤剛力)	|	92963	|	99211	|
|	Vairocana	|	92125	|	99132	|
|	Valanga	|	96060	|	99859	|
|	voltississimo	|	93437	|	99285	|
|	Warriors Aboot	|	95201	|	99639	|
|	ZADAMGA	|	93940	|	99234	|
|	ZETA～素数の世界と超越者～	|	95194	|	99459	|
|	生きてこそ～特別版～	|	96282	|	99635	|
|	一激必翔	|	94907	|	99413	|
|	御千手メディテーション	|	93820	|	99528	|
|	踊るフィーバーロボ	|	93250	|	99397	|
|	カーニバルの主題による人形のためのいびつな狂想曲	|	94012	|	99474	|
|	蛇神	|	95064	|	99758	|
|	金縛りの逢を	|	95573	|	99862	|
|	カラフルトイズ・ワンダーランド	|	94901	|	99511	|
|	カラルの月	|	93564	|	99073	|
|	賢聖シリウスの采配	|	93924	|	99385	|
|	現代のヘイヨエ祭り	|	94875	|	99491	|
|	子供の落書き帳	|	91528	|	99222	|
|	コドモライブ	|	96023	|	99609	|
|	混乱少女♥そふらんちゃん!!	|	90730	|	98976	|
|	流離	|	95049	|	99645	|
|	雫	|	95963	|	99501	|
|	灼熱Beach Side Bunny	|	94800	|	99546	|
|	序	|	93204	|	99095	|
|	少女と時の花	|	95063	|	99239	|
|	人妖絵巻其の三「鴉天狗」～ 鞍馬のHAYATE ～	|	94847	|	99403	|
|	スーパー戦湯ババンバーン	|	94901	|	99587	|
|	翠雨の祷	|	94260	|	99305	|
|	進め！爺ちゃん！	|	88557	|	97460	|
|	西軍||∴⊂SEKIGAHARA⊃∴||東軍	|	93987	|	99692	|
|	青天ノ霹レキ	|	95434	|	99720	|
|	雪上断火	|	96549	|	99458	|
|	創世ノート	|	93875	|	99563	|
|	多極性ニューロンの崩壊による人間の末路	|	93650	|	99556	|
|	たまごの物理科学的 及び調理特性に関しての調査、そしてその考察	|	95524	|	99590	|
|	テンプラ揚三	|	94822	|	99163	|
|	天ぷらイントロドン！！	|	93118	|	99560	|
|	轟け！恋のビーンボール！！	|	95667	|	99601	|
|	バイキングマン	|	93626	|	98800	|
|	背水之陣 (Kagutsuchi Remix)	|	93069	|	99443	|
|	背徳と邪悪のエピタフ	|	93328	|	99524	|
|	万物快楽理論	|	94453	|	99285	|
|	火風陸空	|	96187	|	99730	|
|	風林火山	|	93232	|	99178	|
|	ホーンテッド★メイドランチ	|	94505	|	99647	|
|	ポチコの幸せな日常 (狂犬U`x´UばうわうHARDCORE Remix)	|	93392	|	99373	|
|	ポルターガイスト	|	94135	|	99318	|
|	祭ノ痕、君ヲ憶フ。	|	93898	|	99235	|
|	魔法のかくれんぼ	|	92214	|	98720	|
|	ミサコの告白（みーつけたっ♥）	|	95642	|	99680	|
|	蟲の棲む処	|	94079	|	99110	|
|	夜間行	|	93517	|	98898	|
|	野獣ワイルド	|	95882	|	99894	|
|	夢について　TYPE C	|	95143	|	99702	|
|	龍王の霊廟(Mausoleum Of The Primal Dragon)	|	95927	|	99608	|
|	量子の海のリントヴルム	|	95415	|	99866	|
|	リリーゼと炎龍レーヴァテイン	|	95013	|	99680	|
|	霖が哭く	|	93918	|	99632	|
|	輪廻の鴉	|	95821	|	99741	|
|	霊魂爆砕 -SOUL EXPLOSION-	|	94966	|	99693	|
|	令和の国	|	94197	|	98991	|
|	煉獄事変	|	93348	|	99218	|
|	路男	|	94686	|	99850	|
|	海神	|	96110	|	99832	|

# 参考

下記の内容をとても参考にしました。

・ポックラ一覧を出すスクリプト (作成者:まつまつ様)  
[https://github.com/ssdh233/popn-class](https://github.com/ssdh233/popn-class)  
・BPIとは (作成者:norimiso様)  
[http://norimiso.web.fc2.com/aboutBPI.html](http://norimiso.web.fc2.com/aboutBPI.html)  
