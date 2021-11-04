# Emacs Settings

## How to install emacs26 to ubuntu 18.04
```.sh
$ sudo add-apt-repository ppa:kelleyk/emacs
$ sudo apt update
$ sudo apt install emacs26
```

## How to use MELPA package in emacs
```~/.emacs.d/init.el
;; MELPA
(require 'package)
(add-to-list 'package-archives '("melpa" . "https://melpa.org/packages/"))
(package-initialize)
```

## How to install markdown-mode to emacs
```
M-x package-list-package [ret]
C-s markdown-mode
[ret]
select [install] [ret] y
```
and edit init.el<br>
```~/.emacs.d/init.el
;; markdown-mode
(add-to-list 'auto-mode-alist '("\\.md" . markdown-mode))
```

## Save cursor position
```~/.emacs.d/init.el
(when (require 'saveplace nil t)
  (save-place-mode 1)
  (setq save-place-file "~/.emacs.d/saved-places"))
```
