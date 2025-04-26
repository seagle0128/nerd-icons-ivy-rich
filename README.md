# nerd-icons-ivy-rich

[![CI](https://github.com/seagle0128/nerd-icons-ivy-rich/actions/workflows/ci.yml/badge.svg)](https://github.com/seagle0128/nerd-icons-ivy-rich/actions/workflows/ci.yml)
[![Release Tag](https://img.shields.io/github/tag/seagle0128/nerd-icons-ivy-rich.svg?label=Release)](https://github.com/seagle0128/nerd-icons-ivy-rich/releases)
[![License](http://img.shields.io/:License-GPL3-blue.svg)](License)
[![MELPA](https://melpa.org/packages/nerd-icons-ivy-rich-badge.svg)](https://melpa.org/#/nerd-icons-ivy-rich)
[![MELPA Stable](https://stable.melpa.org/packages/nerd-icons-ivy-rich-badge.svg)](https://stable.melpa.org/#/nerd-icons-ivy-rich)

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->

## Table of Contents

- [Install](#install)
  - [Manual](#manual)
  - [Use-package](#use-package)
- [Customize](#customize)
- [Screenshots](#screenshots)
- [Donate](#donate)

<!-- markdown-toc end -->

Display icons for all buffers in [ivy](https://github.com/abo-abo/swiper).

This package is extracted from [Centaur
Emacs](https://github.com/seagle0128/.emacs.d) and leverages
[ivy-rich](https://github.com/Yevgnen/ivy-rich) and
[nerd-icons](https://github.com/rainstormstudio/nerd-icons.el).

## Install

### Manual

From melpa, `M-x package-install RET nerd-icons-ivy-rich RET`.

```emacs-lisp
(nerd-icons-ivy-rich-mode 1)
(ivy-rich-mode 1)
```

### Use-package

```emacs-lisp
(use-package nerd-icons-ivy-rich
  :ensure t
  :init
  (nerd-icons-ivy-rich-mode 1)
  (ivy-rich-mode 1))
```

_NOTE_:

1. `nerd-icons-ivy-rich-mode` depends on
   [ivy-rich](https://github.com/Yevgnen/ivy-rich) and respects `ivy-rich-mode`.
1. To display icons correctly, you should run `M-x nerd-icons-install-fonts`
   to install the necessary fonts.
1. For better performance, enable `nerd-icons-ivy-rich-mode` before `ivy-rich-mode` .
1. Enable other packages like `counsel-projectile` before enabling `nerd-icons-ivy-rich-mode`.

Enjoy! :smile:

## Customize

```emacs-lisp
;; Whether display the icons
(setq nerd-icons-ivy-rich-icon t)

;; Whether display the colorful icons.
;; It respects `nerd-icons-color-icons'.
(setq nerd-icons-ivy-rich-color-icon t)

;; The icon size
(setq nerd-icons-ivy-rich-icon-size 1.0)

;; Whether support project root
(setq nerd-icons-ivy-rich-project t)

;; Maximum truncation width of annotation fields.
;; This value is adjusted depending on the `window-width'.
(setq nerd-icons-ivy-rich-field-width 80)

;; Definitions for ivy-rich transformers.
;; See `ivy-rich-display-transformers-list' for details."
nerd-icons-ivy-rich-display-transformers-list

;; Slow Rendering
;; If you experience a slow down in performance when rendering multiple icons simultaneously,
;; you can try setting the following variable
(setq inhibit-compacting-font-caches t)
```

In `counsel-describe-function`, `counsel-describe-variable`and `counsel-describe-symbol`, the symbol
classes will be displayed. The details are below.

| Function                   | Variable                                       | Other     |
| -------------------------- | ---------------------------------------------- | --------- |
| f function                 | u custom (U modified compared to global value) | a face    |
| c cooamd                   | v variable                                     | t cl-type |
| C interactive-only command | l local (L modified compared to default value) |           |
| m macto                    | - obsolete                                     |           |
| M special form             |                                                |           |
| g cl-generic               |                                                |           |
| p pure                     |                                                |           |
| s side-effect-free         |                                                |           |
| @ autoloaded               |                                                |           |
| ! advised                  |                                                |           |

## Screenshots

![image](https://user-images.githubusercontent.com/140797/232552947-32feac2a-5eaf-47bf-bf48-3a5ffca9bfc0.png)

![image](https://user-images.githubusercontent.com/140797/232553638-de27aeec-3c4a-421e-a6c1-888cf2d83fa3.png)

![image](https://user-images.githubusercontent.com/140797/232553261-33226017-a487-464e-ba73-227e2bd60159.png)

## Donate

If you think the it's helpful for you, please consider paying a cup of coffee
for me. Thank you! :smile:

<img
src="https://user-images.githubusercontent.com/140797/65818854-44204900-e248-11e9-9cc5-3e6339587cd8.png"
alt="Alipay" width="120"/>
&nbsp;&nbsp;&nbsp;&nbsp;
<img
src="https://user-images.githubusercontent.com/140797/65818844-366ac380-e248-11e9-931c-4bd872d0566b.png"
alt="Wechat Pay" width="120"/>

<a href="https://paypal.me/seagle0128" target="_blank">
<img
src="https://www.paypalobjects.com/digitalassets/c/website/marketing/apac/C2/logos-buttons/optimize/44_Grey_PayPal_Pill_Button.png"
alt="PayPal" width="120" />
</a>
&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://www.buymeacoffee.com/s9giES1" target="_blank">
<img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee"
width="160"/>
</a>
