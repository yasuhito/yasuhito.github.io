+++
title = "org-transclusion"
author = ["Yasuhito Takamiya"]
date = 2021-03-29T00:00:00+09:00
draft = false
+++

[Org Mode]({{< relref "20210223135036-org_mode" >}}) で Roam Research 的なブロック参照を行うためのパッケージ。

[Org-Roam]({{< relref "20210223134834-org_roam" >}}) で書いたノートの一部を、他のノートや [Doom Emacs]({{< relref "20210224132528-doom_emacs" >}}) の config.org から参照したくなったので導入。


## 設定 {#設定}

`~/.doom.d/packages.el` の設定

<a id="code-snippet--org-transclusion configuration (packages.el)"></a>
```emacs-lisp
(package! org-transclusion
  :recipe (:host github
           :repo "nobiot/org-transclusion"
           :branch "main"))
```

`~/.doom.d/config.el` の設定

<a id="code-snippet--org-transclusion configuration (config.el)"></a>
```emacs-lisp
(use-package! org-transclusion
  :hook (org-roam-mode . org-transclusion-mode))
```


## リンク {#リンク}

-   [nobiot/org-transclusion](https://github.com/nobiot/org-transclusion)
