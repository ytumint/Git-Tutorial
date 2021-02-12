# Git Komutları

### Init
*git init* komutu git yapılandırmasını dahil eder.
### Kullanım
    $ git init
    $ git init -b <branch-name>
-----------------

### Config
*git config* komutu git ile alakalı yapılandırmaları belirlemek için kullanılır.
### Kullanım
    $ git config --global user.name "ad soyad"
    $ git config --global user.email "ornek@mail.com"
    $ git config --list
-----------------

### Status
*git status* komutu git kullanarak takip edilen dizindeki dosyaların değişikliklerini listeler.
### Kullanım
    $ git status
    $ git status -s
    $ git branch -b
-----------------

### Add
*git add* komutu değişiklik yaptığımız dosyaları commit edilmek üzere 'stage' alanına eklememizi sağlar.

![Git Workflow](./images/01-add.png "Git Workflow")

### Kullanım
    $ git add .
    $ git add <file-name>
    $ git add <file-path>
    $ git restore --staged <file-name>
-----------------

### Restore
*git restore* komutu değişiklik yaptığımız dosyanın değişikliklerini geri almak için kullanılır.
### Kullanım
    $ git restore <file-name>
-----------------

### Gitignore
*.gitignore* dosyasına dizindeki istemediğimiz veya gerek duymadığımız dosyaları ekleyerek git'e gönderilmesini ve değişikliklerin takip edilmeini engellemiş oluruz.
### Kullanım
    $ touch .gitignore
    $ nano .gitignore
    $ git status
-----------------

### Commit
*git commit* komutu dosyaların o anki durumunu kaydeder ve bir referans noktası oluşturur. Proje ilerledikten sonra isterseniz commit ettiğiniz başka bir noktaya geri dönüş yapmanızı sağlar.

![commit image](./images/01-commit.png "git commit workflow")

### Kullanım
    $ git commit -m 'this is commit message'
    $ git commit -a -m 'mesaj'
    $ git commit --amend -m 'edited commit message'

-----------------
### Tag
*git tag* komutu belirlediğimiz bir commit'i işaret eden referanslardır. 

![Git Tag Image](./images/01-tag.png "Git Tag Image")

### Kullanım
    $ git tag -a -m --list --delete -lw
    $ git tag <tag-name> 
    $ git show <tag-name>
-----------------

### Log
*git log* komutu yapmış olduğumuz commit'leri listeler.
### Kullanım
    $ git log
    $ git log --oneline
    $ git log -all
    $ git log --decorate
    $ git log --graph
    $ git config --global alias.lo 'log --all --graph --decorate --oneline'

-----------------

### Reset
*git reset* komutu bulunduğumuz branch ile ilerideki veya gerideki bir commit'e gitmeyi sağlar.

![reset image](./images/01-reset.png "reset")

### Kullanım 
    $ git reset <commit-hash>
    $ git reset --soft HEAD~1
    $ git reset --hard HEAD~3
    $ git reflog
    $ git reset -i HEAD~4
-----------------

### Revert
*git revert* komutu bir commit'te yaptığımız değişiklikleri iptal edip bu işlemi yaptığınıza dair yeni bir commit oluşturur.

![revert image 1](./images/01-revert.png "Reset image")
![revert image 2](./images/02-revert.png "Revert vs Reset")
### Kullanım
    $ git revert <commit-hash>

-----------------

### Branch
*git branch* bir projede dallanmayı sağlar. Bir projede birden fazla kişi çalışırken kullanılması gerekir.

![Branch image 1](./images/01-branch.png "Branch image 1")
![Branch image 2](./images/02-branch.png "Branch image 2")

### Kullanım
    $ git branch <new_branch>
    $ git checkout <new_branch>
    $ git branch -d <branch-name>
    $ git branch -M <new_branch>

-----------------

### Checkout ve Switch
*git checkout* komutu branch'ler arasında geçiş yapmamızı ve istediğimiz bir commit'e gidip dosyaların o anki durumunu görmemizi sağlar.

![Checkout](./images/02-checkout.png "Checkout")

![Checkout vs Switch](./images/01-checkout.png "Checkout vs Switch")

### Kullanım
    $ git checkout <commit-hash>
    $ git checkout <branch-name>
    $ git switch <branch-name>

-----------------

### Diff
*git diff* komutu bir dosyadaki farklılıkları görmek için kullanılır.
### Kullanım
    $ git diff
    $ git diff <file-name>
    $ git diff <commit-hash> <commit-hash>
    $ git diff <branch-name> <branch-name>
    $ git diff <branch-name> <branch-name> <file-name>

-----------------

### Merge
*git merge* komutu branchleri birleştirmek için kullanılır. Conflict meydana geldiğinde bunun çözülmesi kullanıcının sorumluluğundadır.

![Merge image 1](./images/01-merge.png "Merge image 1")
![Merge image 2](./images/02-merge.png "Merge image 2")

### Kullanım
    $ git merge <branch-name>
    $ git merge --continue
    $ git merge --abort

-----------------

### Rebase
*git rebase* komutunu kullandığımızda A branchindeki her bir commit B dalına sanki commit işlemi B dalında yapılmış gibi yeniden yazılır.

![Rebase image 1](./images/01-rebase.png "Rebase image 1")

### Kullanım
    $ git rebase <branch-name>

-----------------
### Remote
*git remote* yerel depo ile takip edilen uzak depoyu kontrol edebilmeyi sağlar.

![Remote image 1](./images/01-remote.png "Remote image 1")

### Kullanım
    $ git remove -v 
    $ git remote add <remote-name> <remote-url>
    $ git remote remove <remote-name>
    $ git remote set-url origin git@github.com:USERNAME/REPOSITORY.git.

-----------------
### Clone
*git clone* Github'da varolan bir depoyu tüm dosyalar, dallar dahil olmak üzere klonlar(indirir).
### Kullanım
    $ git clone <remote-url>

-----------------

### Pull
*git pull* içerisinde bulunulan branch'in remote reposundaki değişikler ile bütün commitleri alarak günceller.
### Kullanım
    $ git pull
    $ git pull --rebase
    $ git pull --force
    $ git pull --all

-----------------

### Push
*git push* lokal branchteki commitleri remote repoya yükler.
### Kullanım
    $ git push -u <remote-name> <branch-name>
    $ git push --all
    $ git push --tags
    
-----------------

### Git Workflow

![Git Workflow 1](./images/01-git-workflow.png "Git Workflow 1")

![Git Workflow 2](./images/02-git-workflow.png "Git Workflow 2")

![Git Workflow 3](./images/03-git-workflow.png "Git Workflow 3")
