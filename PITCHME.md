---?color=linear-gradient(to right, #c02425, #f0cb35)
@title[Introduction]

@snap[west headline text-white span-70]
符号化と復号
@snapend

@snap[south-west byline  text-white]
Arch B4 u-dory
@snapend

---

@title[Slide Markdown]

### Each slide in this presentation is provided as a *template*.

<br><br>

1. Select only the slide templates that you need.
1. Customize the template _markdown content_.
1. Optionally, override template _styles_ and _settings_.
1. Then present and publish with GitPitch @fa[smile-o]

<br><br>

---

### 画像の符号化

<br><br>

- 予測符号化
- 変換符号化
- ベクトル量子化
- エントロピー符号化

エントロピー量子化以外は画像の特徴を見越して行われる。

<br><br>

+++

#### 予測符号化

自然画像は隣接する画素に強い相関がみられることが多い。
したがって画素の情報を直接保存するよりも、
隣接する画素から次の画素の値を予測し、実際の値との差分を保存するほうが効率が良くなる。

- 一次元予測
- 二次元予測
  - 平面予測
  - 平均予測

+++

#### 変換符号化

<br><br>

自然画像は隣接する画素に強い相関が(ry
この特性を活かして画素の行列の変換を行うことで情報量を下げる。

- 離散フーリエ変換
- 離散コサイン変換

<br><br>

+++

#### ベクトル量子化

<br><br>

画像をブロックに分け、それと似たサンプルをコードブックから選び出す。
復元する際はコードブックのサンプルを組み合わせることで近似した画像が得られる。

<br><br>

+++

#### エントロピー符号化

<br><br>

データそのものを数学的に符号化する

- ハフマン符号化
- 算術符号化

<br><br>

---

### 予測符号化


近隣の画素から目的画素の値を予測し、実際の画素の値との差を符号とする方法。

- 一次元予測
  - 前値予測
- 二次元予測
  - 行列予測
  - 平均予測
  - 平面予測

+++

#### 前置予測

<br><br>

`\[
{X = A}
\]`

<br><br>

+++

#### 行列予測

<br><br>

`\[
\left( X = (A + C) \over 2 )
\]`

<br><br>