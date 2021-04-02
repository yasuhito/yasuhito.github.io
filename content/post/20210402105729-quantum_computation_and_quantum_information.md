+++
title = "Quantum Computation and Quantum Information"
author = ["Yasuhito Takamiya"]
date = 2021-04-02T00:00:00+09:00
draft = false
+++

{{< figure src="/ox-hugo/2021-04-02_11-15-53_screenshot.png" >}}


## 演習 {#演習}


### 2.1 {#2-dot-1}

ベクトル \\((1, -1)\\), \\((1, 2)\\) および \\((2, 1)\\) は

\begin{equation}
  \begin{bmatrix}
    2 \\\\\\
    1
  \end{bmatrix} =
  \begin{bmatrix}
    1 \\\\\\
    {-1}
  \end{bmatrix} +
  \begin{bmatrix}
    1 \\\\\\
    2
  \end{bmatrix}
\end{equation}

を満たすので、これら 3 つのベクトルは[線形従属]({{< relref "20210331120144-線形従属" >}})。


### 2.2 {#2-dot-2}


#### \\(A\\) の行列表現 {#a--の行列表現}

次のように[演算子は行列で表現できる]({{< relref "20210401104202-演算子は行列て表現てきる" >}})ことから、

\\[A|v\_j\rangle = \sum\_i A\_{ij}|w\_i\rangle\\]

\\(j = 1\\) のとき、

\begin{eqnarray}
  A|0\rangle &=& \sum\_i A\_{i1}|w\_i\rangle \\\\\\
             &=& A\_{11}|0\rangle + A\_{21}|1\rangle
\end{eqnarray}

\\(j = 2\\) のとき、

\begin{eqnarray}
  A|1\rangle &=& \sum\_i A\_{i2}|w\_i\rangle \\\\\\
             &=& A\_{12}|0\rangle + A\_{22}|1\rangle
\end{eqnarray}

これらと \\(A|0\rangle = |1\rangle,\ A|1\rangle = |0\rangle\\) より、

\\(A\_{11} = 0\\), \\(A\_{21} = 1\\), \\(A\_{12} = 1\\), \\(A\_{22} = 0\\)

よって \\(A\\) の行列表現は、

\begin{equation}
  A = \begin{bmatrix}
    0 & 1 \\\\\\
    1 & 0
  \end{bmatrix}
\end{equation}


#### \\(A\\) の異なる行列表現を与える入力と出力の基底 {#a--の異なる行列表現を与える入力と出力の基底}

基底として次を選ぶ:

\begin{eqnarray}
|+\rangle &=& \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) \\\\\\
|-\rangle &=& \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle)
\end{eqnarray}

ここで \\(A|+\rangle\\) と \\(A|-\rangle\\) を計算すると、

\begin{eqnarray}
  A|+\rangle &=& \frac{1}{\sqrt{2}}(A|0\rangle + A|1\rangle) \\\\\\
             &=& \frac{1}{\sqrt{2}}(|1\rangle + |0\rangle) \\\\\\
             &=& |+\rangle
\end{eqnarray}

\begin{eqnarray}
  A|-\rangle &=& \frac{1}{\sqrt{2}}(A|0\rangle - A|1\rangle) \\\\\\
             &=& \frac{1}{\sqrt{2}}(|1\rangle - |0\rangle) \\\\\\
             &=& -|-\rangle
\end{eqnarray}

これらの結果と行列 \\(A\\) の要素 \\(A\_{ij}\\) を求める式から、

\begin{eqnarray}
  A|+\rangle &=& \sum\_i A\_{i1}|w\_i\rangle \\\\\\
             &=& A\_{11}|+\rangle + A\_{21}|-\rangle \\\\\\
             &=& |+\rangle
\end{eqnarray}

\begin{eqnarray}
  A|-\rangle &=& \sum\_i A\_{i2}|w\_i\rangle \\\\\\
             &=& A\_{12}|+\rangle + A\_{22}|-\rangle \\\\\\
             &=& -|-\rangle
\end{eqnarray}

よって \\(A\_{11} = 1\\), \\(A\_{21} = 0\\), \\(A\_{12} = 0\\), \\(A\_{22} = -1\\) となり、\\(A\\) の行列表現は

\begin{equation}
  A = \begin{bmatrix}
    1 & 0 \\\\\\
    0 & -1
  \end{bmatrix}
\end{equation}

となるので、確かに異なる行列表現を持つ。


## 先人達の回答例 {#先人達の回答例}

-   [goropikari/SolutionQCQINielsenChuang](https://github.com/goropikari/SolutionQCQINielsenChuang)
-   [Solutions: Quantum Computation and Quantum Information by Nielsen and Chuang](https://serab.net/docs/qcqi/)
-   [QCQI Exercise Solutions (Index)](https://enakai00.hatenablog.com/entry/2018/04/22/195026)
