# Emacs Ultimate guide 

* Help

** Emacs tutorial 
   - C-h t

** Emacs keyword/expression help
   - C-h f

** Emacs key help
   - C-h k


* Buffers 

** To create buffer or use buffer
   - C-x b

** To list buffer in different window
   - C-x C-b

** to kill buffer
   - C-x k

** 


* Setting up ido-mode
  - (setq ido-enable-flex-matching t)
  - (setq ido-everywhere t)
  - (ido-mode 1)

* setting up ibuffer window ( a somewhat better version of buffer windows)
  - (defalias 'list-buffers 'ibuffer)
  - (defalias 'list-buffers 'ibuffer-other-window)
** Controls
   _ D - to mark buffers for deletion
   _ X - execute buffers with D
   _ C-d - to mark buffers (and so on...)



* Settiing up 
  - (use-package tabbar
\  - :ensure t
  - :config
  - (tabbar-mode 1))

* Windows in emacs

** switch window
   - C-x o
** close window 
   - C-x 0
** close every window except current
   - C-x 1
** split  new window horizontally
   - C-x 2
** split new window vertically
   - C-x 3

** using winnder mode
   - (winner-mode 1)
     * it'll allow undo redo windows config with commands
       - C-c left-key (undo) or C-c right-key (redo)
** Setting up ace-window ( for making windows switching convenient)
   - C-x o <window-number>
   - (use-package ace-window
     :ensure t
     :init
     (progn
        (global--key [remap other-window] 'ace-window)
    ))

Note:- C-q/M-q (wraps the para)

* Search (common)
** to search
   _ C-s <word>
** to find next word
   _ C-s
** to find previous word
   _ C-r

* Swiper Search
  - We'll be using swiper which is more convenient than search
  - it also have support for C-x C-f find file option
  - swiper also support regex search right away for bried controls description visit the documentation page
  - copy the code from the swiper official repo (github.com/abo-abo/swiper) and paste it 
    - (use-package swiper
        :ensure t
	:config t
	(progn
	  <paste-swiper-code>
	  ))

** Common Swiper Controls
   - search (C-s)
   - next (C-n)
   - previous (C-p)
   - supprot space as a wild card

** embedding swiper in find-file
   - install counsel package before swiper as it is a dependency 
   - (use-package counsel
       :ensure t
       )






