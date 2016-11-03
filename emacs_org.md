# org mode 介紹

## 總體介紹

- 作爲一個曾經的vimer 讓我轉向emacs 的主要原因就是org mode. 同樣作爲make up language，在 org mode 下可以輕鬆地實現 markdown中的所有效果， 但它更強的功能是在於GTD管理,和強大的導出功能.

## 用org mode做GTD

- 在org mode中在任意的一行按下C c C t 就可以讓這行文字作爲代辦事宜在To Do 和Done 之間切換，而按下C c C s則可以爲這件待辦事宜設置準備完成的時間。在安裝了org aganda之後，無論你在編輯什麼文件時候都可以打開 org aganda 查看自己還有什麼事情沒有完成。如果你是在mac os下使用emacs 你甚至可以把所有待辦事宜導出爲icandeler文件,配合icanderler 使用。
- 在使用了org mode之後，我現在每天打開電腦第一件事情就是按下C a o a查看自己的今天的安排是什麼。在我每天做完了任何事情之後也是先把org 文件的那一項事物改爲Done 並且記錄下心得順便查看完成的時間。 
- 除了這些常規的GTD功能之外，org mode 還提供把某個事項設置爲重復的功能，只需要在設置的之後加入+1d 或者+1w 就可以把這個事項設置爲每天或每周重復，這可以提醒你完成一些固定項目比如我就是把每天的運動和每周的水電費繳納時間都寫在了我的habit.org 中，這樣就不用再花太多的精力在記憶日常的瑣事上面了。

## org mode 強大導出功能

- org 文件在emacs 中可以導出成爲html，latex， pdf等文件，其中pdf文件是先把org 文件輸出爲tex 文件再通過pdflatex輸出爲pdf文件。
- 在把org文件export 爲不同文件時，可以自行添加文件頭。在org 文件頭中設置了引入css文件後，我們可以修改生成html的樣式.我的[個人wiki](http://markwh1te.github.io/)就是用這種辦法生成的, 而且由於是直接放在github 可以通過github pages直接訪問並且可以直接登錄github在網站上修改，隨時更新就可以隨時看到結果，十分適合隨時都有可能改動wiki.

## 雙刃劍

- org mode 還有很多強大的功能，比如代碼運行和表格求值等等，但是也有美中不足的地方，那就是依賴於emacs ，由於emacs 有一定的學習難度，所以這也是很多人不知道org mode 一個原因。就像我感覺haskell 應該是這個世界上最完美的編程語言，但是在實際應用中卻並不常見，不是應爲haskell 不強大，而是願意沉下心來學習它理解它的人太少。
- 雖然org mode 使用的人數沒有markdown多，支持的平臺也只有emacs 但是它確實有值得學習的地方是一個很值得點亮的技能點， 我現在就是GTD和wiki使用org ，寫blog和灌水使用markdown ，同時使用這兩種makeup language.在合適地方使用合適的語言。
