什么是branch？

需求是开发的起点，先有需求再有功能分支（feature branch）或者补丁分支（hotfix branch）。完成开发后，该分支就合并到主分支，然后被删除。分支一般有发布环境分支（master），预发环境分支（release branch），开发分支（develop branch），功能分支（feature branch），补丁分支（hotfix branch）等。分支的意义在于：为了在开发的同时又能保证master的稳健型，一旦完成开发，它们就会被合并进develop或master，然后被删除。
