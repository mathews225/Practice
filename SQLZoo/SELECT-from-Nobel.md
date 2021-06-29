<div id="bodyContent" class="mw-body-content">
		
		
		
		
		
<tbody><tr style="background:#EEF3E2">
<th class="mbox-image" style="white-space:nowrap; padding:4px 1em; border-right:1px solid #aaa"> <a href="/wiki/Special:MyLanguage/Project:Language_policy" title="Special:MyLanguage/Project:Language policy">Language:</a><span style="display:none"><a href="/wiki/SQLZOO:Language_policy" title="SQLZOO:Language policy">Project:Language policy</a></span></th>
<td class="mbox-text" style="background:#F6F9ED"><b><a class="mw-selflink selflink">English</a></b> &nbsp;• <bdi lang="ja"><a href="/wiki/SELECT_from_Nobel_Tutorial/ja" title="SELECT from Nobel Tutorial/ja">日本語</a></bdi><span class="autonym"></span><span class="autonym"></span>&nbsp;• <bdi lang="zh"><a href="/wiki/SELECT_from_Nobel_Tutorial/zh" title="SELECT from Nobel Tutorial/zh">中文</a></bdi></td>
</tr></tbody></table>
<div class="ref_section" style="float:right">
<table class="db_ref">
<caption>nobel</caption>
<tbody><tr><th>yr</th>
<th>subject</th>
<th>winner</th>
</tr><tr>
<td>1960</td>
<td>Chemistry</td>
<td align="left">Willard F. Libby</td>
</tr>
<tr>
<td>1960</td>
<td>Literature</td>
<td align="left">Saint-John Perse</td>
</tr>
<tr>
<td>1960</td>
<td>Medicine</td>
<td align="left">Sir Frank Macfarlane Burnet</td>
</tr>
<tr>
<td>1960</td>
<td>Medicine</td>
<td align="left">Peter Madawar</td>
</tr>
<tr>
<td colspan="5">...</td>
</tr>
</tbody></table>
</div>
  <div id="toc" class="toc"><input type="checkbox" role="button" id="toctogglecheckbox" class="toctogglecheckbox" style="display:none"><div class="toctitle" lang="en" dir="ltr"><h2>Contents</h2><span class="toctogglespan"><label class="toctogglelabel" for="toctogglecheckbox"></label></span></div>
<ul>
<li class="toclevel-1"><a href="#nobel_Nobel_Laureates"><span class="tocnumber">1</span> <span class="toctext">nobel Nobel Laureates</span></a></li>
<li class="toclevel-1 tocsection-1"><a href="#Winners_from_1950"><span class="tocnumber">2</span> <span class="toctext">Winners from 1950</span></a></li>
<li class="toclevel-1 tocsection-2"><a href="#1962_Literature"><span class="tocnumber">3</span> <span class="toctext">1962 Literature</span></a></li>
<li class="toclevel-1 tocsection-3"><a href="#Albert_Einstein"><span class="tocnumber">4</span> <span class="toctext">Albert Einstein</span></a></li>
<li class="toclevel-1 tocsection-4"><a href="#Recent_Peace_Prizes"><span class="tocnumber">5</span> <span class="toctext">Recent Peace Prizes</span></a></li>
<li class="toclevel-1 tocsection-5"><a href="#Literature_in_the_1980.27s"><span class="tocnumber">6</span> <span class="toctext">Literature in the 1980's</span></a></li>
<li class="toclevel-1 tocsection-6"><a href="#Only_Presidents"><span class="tocnumber">7</span> <span class="toctext">Only Presidents</span></a></li>
<li class="toclevel-1 tocsection-7"><a href="#John"><span class="tocnumber">8</span> <span class="toctext">John</span></a></li>
<li class="toclevel-1 tocsection-8"><a href="#Chemistry_and_Physics_from_different_years"><span class="tocnumber">9</span> <span class="toctext">Chemistry and Physics from different years</span></a></li>
<li class="toclevel-1 tocsection-9"><a href="#Exclude_Chemists_and_Medics"><span class="tocnumber">10</span> <span class="toctext">Exclude Chemists and Medics</span></a></li>
<li class="toclevel-1 tocsection-10"><a href="#Early_Medicine.2C_Late_Literature"><span class="tocnumber">11</span> <span class="toctext">Early Medicine, Late Literature</span></a></li>
<li class="toclevel-1 tocsection-11"><a href="#Harder_Questions"><span class="tocnumber">12</span> <span class="toctext">Harder Questions</span></a></li>
<li class="toclevel-1 tocsection-12"><a href="#Umlaut"><span class="tocnumber">13</span> <span class="toctext">Umlaut</span></a></li>
<li class="toclevel-1 tocsection-13"><a href="#Apostrophe"><span class="tocnumber">14</span> <span class="toctext">Apostrophe</span></a></li>
<li class="toclevel-1 tocsection-14"><a href="#Knights_of_the_realm"><span class="tocnumber">15</span> <span class="toctext">Knights of the realm</span></a></li>
<li class="toclevel-1 tocsection-15"><a href="#Chemistry_and_Physics_last"><span class="tocnumber">16</span> <span class="toctext">Chemistry and Physics last</span></a></li>
</ul>
</div>

<h2><span class="mw-headline" id="nobel_Nobel_Laureates"><code>nobel</code> Nobel Laureates</span></h2>
  <p>We continue practicing simple SQL queries on a single table.</p>
  <p>This tutorial is concerned with a table of Nobel prize winners:
  </p>
  <pre style="width:20em;">nobel(yr, subject, winner)</pre>
<p>Using the <code>SELECT</code> statement.<br><br><br></p>


## Winners from 1950

_Change the query shown so that it displays Nobel prizes for 1950._


```sql
SELECT yr, subject, winner
FROM nobel
WHERE yr = 1950
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1950</td><td>Chemistry</td><td>Kurt Alder</td></tr><tr><td class="r">1950</td><td>Chemistry</td><td>Otto Diels</td></tr><tr><td class="r">1950</td><td>Literature</td><td>Bertrand Russell</td></tr><tr><td class="r">1950</td><td>Medicine</td><td>Edward C. Kendall</td></tr><tr><td class="r">1950</td><td>Medicine</td><td>Philip S. Hench</td></tr><tr><td class="r">1950</td><td>Medicine</td><td>Tadeus Reichstein</td></tr><tr><td class="r">1950</td><td>Peace</td><td>Ralph Bunche</td></tr><tr><td class="r">1950</td><td>Physics</td><td>Cecil Powell</td></tr></table>



## 1962 Literature
_Show who won the 1962 prize for Literature._

```sql
SELECT winner
  FROM nobel
 WHERE yr = 1962
   AND subject = 'Literature'
```

### Correct answer
<table class="sqlmine"><tr><th>winner</th></tr><tr><td>John Steinbeck</td></tr></table></div></div>



## Albert Einstein

_Show the year and subject that won 'Albert Einstein' his prize._

```sql
SELECT
  yr
  , subject
FROM nobel
WHERE winner LIKE 'Albert Einstein';
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th></tr><tr><td class="r">1921</td><td>Physics</td></tr></table>



## Recent Peace Prizes
Give the name of the 'Peace' winners since the year 2000, including 2000.

```sql
SELECT
  winner
FROM nobel
WHERE
  subject LIKE 'Peace'
   AND
  yr >= 2000;
```

### Correct answer
<table class="sqlmine"><tr><th>winner</th></tr><tr><td>Kim Dae-jung</td></tr><tr><td>Kofi Annan</td></tr><tr><td>United Nations</td></tr><tr><td>Jimmy Carter</td></tr><tr><td>Shirin Ebadi</td></tr><tr><td>Wangari Maathai</td></tr><tr><td>International Atomic Energy Agency</td></tr><tr><td>Mohamed ElBaradei</td></tr><tr><td>Grameen Bank</td></tr><tr><td>Muhammad Yunus</td></tr><tr><td>Al Gore</td></tr><tr><td>Intergovernmental Panel on Climate Change</td></tr><tr><td>Martti Ahtisaari</td></tr><tr><td>Barack Obama</td></tr><tr><td>Liu Xiaobo</td></tr><tr><td>Ellen Johnson Sirleaf</td></tr><tr><td>Leymah Gbowee</td></tr><tr><td>Tawakel Karman</td></tr><tr><td>European Union</td></tr><tr><td>Kailash Satyarthi</td></tr><tr><td>Malala Yousafzai</td></tr><tr><td>Tunisian National Dialogue Quartet</td></tr><tr><td>Juan Manuel Santos</td></tr><tr><td>International Campaign to Abolish Nuclear Weapons</td></tr></table>



## Literature in the 1980's

_Show all details of the Literature prize winners for 1980 to 1989 inclusive._

```sql
SELECT
  yr
  , subject
  , winner
FROM nobel
WHERE
  subject LIKE 'Literature'
   AND
  yr BETWEEN 1980 AND 1989;
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1980</td><td>Literature</td><td>Czeslaw Milosz</td></tr><tr><td class="r">1981</td><td>Literature</td><td>Elias Canetti</td></tr><tr><td class="r">1982</td><td>Literature</td><td>Gabriel García Márquez</td></tr><tr><td class="r">1983</td><td>Literature</td><td>William Golding</td></tr><tr><td class="r">1984</td><td>Literature</td><td>Jaroslav Seifert</td></tr><tr><td class="r">1985</td><td>Literature</td><td>Claude Simon</td></tr><tr><td class="r">1986</td><td>Literature</td><td>Wole Soyinka</td></tr><tr><td class="r">1987</td><td>Literature</td><td>Joseph Brodsky</td></tr><tr><td class="r">1988</td><td>Literature</td><td>Naguib Mahfouz</td></tr><tr><td class="r">1989</td><td>Literature</td><td>Camilo José Cela</td></tr></table>



## Only Presidents

_Show all details of the presidential winners._

- Theodore Roosevelt
- Woodrow Wilson
- Jimmy Carter
- Barack Obama


```sql
SELECT * FROM nobel
WHERE 
  winner IN (
   'Theodore Roosevelt'
   , 'Woodrow Wilson'
   , 'Jimmy Carter'
   , 'Barack Obama')
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1906</td><td>Peace</td><td>Theodore Roosevelt</td></tr><tr><td class="r">1919</td><td>Peace</td><td>Woodrow Wilson</td></tr><tr><td class="r">2002</td><td>Peace</td><td>Jimmy Carter</td></tr><tr><td class="r">2009</td><td>Peace</td><td>Barack Obama</td></tr></table>




## John
_Show the winners with first name John._

```sql
SELECT winner
FROM nobel
WHERE
  winner LIKE 'John %';
```

### Correct answer
<table class="sqlmine"><tr><th>winner</th></tr><tr><td>John Macleod</td></tr><tr><td>John Galsworthy</td></tr><tr><td>John H. Northrop</td></tr><tr><td>John R. Mott</td></tr><tr><td>John Cockcroft</td></tr><tr><td>John F. Enders</td></tr><tr><td>John Bardeen</td></tr><tr><td>John C. Kendrew</td></tr><tr><td>John Steinbeck</td></tr><tr><td>John R. Hicks</td></tr><tr><td>John Bardeen</td></tr><tr><td>John Cornforth</td></tr><tr><td>John H. van Vleck</td></tr><tr><td>John R. Vane</td></tr><tr><td>John C. Polanyi</td></tr><tr><td>John C. Harsanyi</td></tr><tr><td>John F. Nash Jr.</td></tr><tr><td>John E. Walker</td></tr><tr><td>John Pople</td></tr><tr><td>John Hume</td></tr><tr><td>John B. Fenn</td></tr><tr><td>John E. Sulston</td></tr><tr><td>John L. Hall</td></tr><tr><td>John C. Mather</td></tr><tr><td>John B. Gurdon</td></tr><tr><td>John O'Keefe</td></tr><tr><td>John M. Kosterlitz</td></tr></table>



## Chemistry and Physics from different years

_Show the year, subject, and name of Physics winners for 1980 together with the Chemistry winners for 1984._


```sql
SELECT * FROM nobel
WHERE (subject like 'Physics' 
        AND
       yr = 1980)
    OR
      (subject like 'Chemistry' 
        AND
       yr = 1984);
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1980</td><td>Physics</td><td>James Cronin</td></tr><tr><td class="r">1980</td><td>Physics</td><td>Val Fitch</td></tr><tr><td class="r">1984</td><td>Chemistry</td><td>Bruce Merrifield</td></tr></table>



## Exclude Chemists and Medics
_Show the year, subject, and name of winners for 1980 excluding Chemistry and Medicine_

```sql
SELECT * FROM nobel
WHERE (yr = 1980)
    AND NOT
      (subject like 'Chemistry' 
        or 
       subject like 'Medicine');
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1980</td><td>Economics</td><td>Lawrence R. Klein</td></tr><tr><td class="r">1980</td><td>Literature</td><td>Czeslaw Milosz</td></tr><tr><td class="r">1980</td><td>Peace</td><td>Adolfo Pérez Esquivel</td></tr><tr><td class="r">1980</td><td>Physics</td><td>James Cronin</td></tr><tr><td class="r">1980</td><td>Physics</td><td>Val Fitch</td></tr></table>



## Early Medicine, Late Literature
_Show year, subject, and name of people who won a 'Medicine' prize in an early year (before 1910, not including 1910) together with winners of a 'Literature' prize in a later year (after 2004, including 2004)_


```sql
SELECT * FROM nobel
WHERE (subject like 'Medicine' 
        AND 
       yr < 1910)
    OR
      (subject like 'Literature' 
        AND yr >= 2004);
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1901</td><td>Medicine</td><td>Emil von Behring</td></tr><tr><td class="r">1902</td><td>Medicine</td><td>Ronald Ross</td></tr><tr><td class="r">1903</td><td>Medicine</td><td>Niels Ryberg Finsen</td></tr><tr><td class="r">1904</td><td>Medicine</td><td>Ivan Pavlov</td></tr><tr><td class="r">1905</td><td>Medicine</td><td>Robert Koch</td></tr><tr><td class="r">1906</td><td>Medicine</td><td>Camillo Golgi</td></tr><tr><td class="r">1906</td><td>Medicine</td><td>Santiago Ramón y Cajal</td></tr><tr><td class="r">1907</td><td>Medicine</td><td>Alphonse Laveran</td></tr><tr><td class="r">1908</td><td>Medicine</td><td>Ilya Mechnikov</td></tr><tr><td class="r">1908</td><td>Medicine</td><td>Paul Ehrlich</td></tr><tr><td class="r">1909</td><td>Medicine</td><td>Theodor Kocher</td></tr><tr><td class="r">2004</td><td>Literature</td><td>Elfriede Jelinek</td></tr><tr><td class="r">2005</td><td>Literature</td><td>Harold Pinter</td></tr><tr><td class="r">2006</td><td>Literature</td><td>Orhan Pamuk</td></tr><tr><td class="r">2007</td><td>Literature</td><td>Doris Lessing</td></tr><tr><td class="r">2008</td><td>Literature</td><td>Jean-Marie Gustave Le Clézio</td></tr><tr><td class="r">2009</td><td>Literature</td><td>Herta Müller</td></tr><tr><td class="r">2010</td><td>Literature</td><td>Mario Vargas Llosa</td></tr><tr><td class="r">2011</td><td>Literature</td><td>Tomas Tranströmer</td></tr><tr><td class="r">2012</td><td>Literature</td><td>Mo Yan</td></tr><tr><td class="r">2013</td><td>Literature</td><td>Alice Munro</td></tr><tr><td class="r">2014</td><td>Literature</td><td>Patrick Modiano</td></tr><tr><td class="r">2015</td><td>Literature</td><td>Svetlana Alexievich</td></tr><tr><td class="r">2016</td><td>Literature</td><td>Bob Dylan</td></tr><tr><td class="r">2017</td><td>Literature</td><td>Kazuo Ishiguro</td></tr></table>



# Harder Questions


## Umlaut
_Find all details of the prize won by PETER GRÜNBERG._

```sql
SELECT * FROM nobel
WHERE 
  winner LIKE 'PETER GR_NBERG';
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">2007</td><td>Physics</td><td>Peter Grünberg</td></tr></table>



## Apostrophe
_Find all details of the prize won by EUGENE O'NEILL._

```sql
SELECT * FROM nobel
WHERE 
  winner LIKE 'EUGENE O_NEILL';
```

### Correct answer
<table class="sqlmine"><tr><th>yr</th><th>subject</th><th>winner</th></tr><tr><td class="r">1936</td><td>Literature</td><td>Eugene O'Neill</td></tr></table>

## Knights of the realm
_Knights in order_

_List the winners, year and subject where the winner starts with Sir. Show the the most recent first, then by name order._

```sql
SELECT
  winner
  , yr
  , subject
FROM nobel
WHERE
  winner LIKE 'Sir%'
ORDER BY 
  yr DESC
  , winner
```

### Correct answer
<table class="sqlmine"><tr><th>winner</th><th>yr</th><th>subject</th></tr><tr><td>Sir Martin J. Evans</td><td class="r">2007</td><td>Medicine</td></tr><tr><td>Sir Peter Mansfield</td><td class="r">2003</td><td>Medicine</td></tr><tr><td>Sir Paul Nurse</td><td class="r">2001</td><td>Medicine</td></tr><tr><td>Sir Harold Kroto</td><td class="r">1996</td><td>Chemistry</td></tr><tr><td>Sir James W. Black</td><td class="r">1988</td><td>Medicine</td></tr><tr><td>Sir Arthur Lewis</td><td class="r">1979</td><td>Economics</td></tr><tr><td>Sir Nevill F. Mott</td><td class="r">1977</td><td>Physics</td></tr><tr><td>Sir Bernard Katz</td><td class="r">1970</td><td>Medicine</td></tr><tr><td>Sir John Eccles</td><td class="r">1963</td><td>Medicine</td></tr><tr><td>Sir Frank Macfarlane Burnet</td><td class="r">1960</td><td>Medicine</td></tr><tr><td>Sir Cyril Hinshelwood</td><td class="r">1956</td><td>Chemistry</td></tr><tr><td>Sir Robert Robinson</td><td class="r">1947</td><td>Chemistry</td></tr><tr><td>Sir Alexander Fleming</td><td class="r">1945</td><td>Medicine</td></tr><tr><td>Sir Howard Florey</td><td class="r">1945</td><td>Medicine</td></tr><tr><td>Sir Henry Dale</td><td class="r">1936</td><td>Medicine</td></tr><tr><td>Sir Norman Angell</td><td class="r">1933</td><td>Peace</td></tr><tr><td>Sir Charles Sherrington</td><td class="r">1932</td><td>Medicine</td></tr><tr><td>Sir Venkata Raman</td><td class="r">1930</td><td>Physics</td></tr><tr><td>Sir Frederick Hopkins</td><td class="r">1929</td><td>Medicine</td></tr><tr><td>Sir Austen Chamberlain</td><td class="r">1925</td><td>Peace</td></tr><tr><td>Sir William Ramsay</td><td class="r">1904</td><td>Chemistry</td></tr></table>


## Chemistry and Physics last
_The expression subject IN ('Chemistry','Physics') can be used as a value - it will be 0 or 1._

_Show the 1984 winners and subject ordered by subject and winner name; but list Chemistry and Physics last._

```sql
SELECT winner, subject
  FROM nobel
 WHERE yr=1984
 ORDER BY
    (CASE 
      WHEN subject IN ('Physics', 'Chemistry') THEN 1 
      ELSE 0 
    END)
   , subject
   , winner;
```

### Result:
<table class="sqlmine"><tr><th>winner</th><th>subject</th></tr><tr><td>Richard Stone</td><td>Economics</td></tr><tr><td>Jaroslav Seifert</td><td>Literature</td></tr><tr><td>César Milstein</td><td>Medicine</td></tr><tr><td>Georges J.F. Köhler</td><td>Medicine</td></tr><tr><td>Niels K. Jerne</td><td>Medicine</td></tr><tr><td>Desmond Tutu</td><td>Peace</td></tr><tr><td>Bruce Merrifield</td><td>Chemistry</td></tr><tr><td>Carlo Rubbia</td><td>Physics</td></tr><tr><td>Simon van der Meer</td><td>Physics</td></tr></table>

</div>