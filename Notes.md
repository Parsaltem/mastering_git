https://www.youtube.com/watch?v=S7XpTAnSDL4

## Versiyon Kontrolü için
git version --

## Update için
git update

## Github bilgilerinin güncellenmesi için
- git config --global credential.helper store
- git pull

## Kullanıcı adı ve mail için
- git config --global user.name 'parsaltem'
- git config --global user.email 'altemuraltan@hotmail.com'

## Git'e entegre klasör oluşturmak için, klasörün içindeyken terminalde
- git init
- git config --global init.defaultBranch main
- git init

## Dosyaları oluşturduktan sonra (aynı zamanda dosyalar üzerinde ne işlem yapıldığıyla iligi olarak)
git status

## Git'e dosyayı göndermek için
- git add **dosya adı*
- git commit -m 'Add notes.txt file' (commit öyle olmalı ki ileride bi hata olduğunda bu commite geri dönebilesin - Tarih eklemek mantıklı)

## tüm dosyaları göndermek için
git add ./

## tüm dosyalara commit için
git commit -m 'tarih eklemek mantıklı'

## tüm yapılan işleri görmek için 
git log

## Log verisinde çıkan rakamlarla geriye istediğin gibi dönmek mümkün.
git checkout 7e7f35d3577ddbb7004b8acbf1666783dc7aac76 ##Bu komutla eski versiyonlara dönebiliyorsun.

## Son versiyona dönmek için ise 
- git checkout main 
- git checkout -f main

## GITHUB
www.github.com'da new reporistory oluştur. (Klasör oluşturmak gibi)

## terminalde 
git branch -M main

## Github'a dosyaları göndermek için
- git remote add origin https://github.com/Parsaltem/mastering_git.git
- git push -u origin main

# *BRANCHING & MERGING*

## branch oluşturmak için
git branch branch-name

## bu branch'de çalışmak için
git checkout branch-name

## Ana dosya'da çalışmak için
git checkout main

## branch oluşturduktan sonra direkt olarak bu branche gitmek için
git checkout -b feature-branch

## branch altında branch oluşturmak için
git branch branch-name another-branch-name

## GitHub branch'i senkronize etmek için
- git push --set-upstream origin feature-branch
- git push -u origin feature-branch

## Branch altında biri branch oluşturursa bunu locale çekmek için
git pull

## GitHub'da Yapılacaklar
- Pull Request
- New Pull Request
- base:Main compare:feature-brach

Birleştirdikten sonra alt branch^leri silebiliriz.

## Terminal'de yapılacak.
git pull

## İlk Kısım Notları
 1. Clone the repository
 2. Create a new branch from the main or another branch
 3. Make your changes
 4. Push the branch to the remote repo
 5. Open a Pull Request
 6. Merge the changes
 7. Pull the merged changes into your local main branch
 8. Repeat from step 2

# *MERGING CONFLICT*

- 2 branch oluşturuyorsun.
- branchlerden pull request geliyor.
- birini kabul ediyorsun.
- diğeri çakışıyor.

# *RESET* 43:30

 - 3 Türü mevcut:
 1. Soft : Sonraki değişiklikleri görebiliyorsun.   git reset --soft 7e7f35d3577ddbb7004b8acbf1666783dc7aac76
 2. Hard : Sonraki değişiklikleri göremiyorsun.     git reset --hard 7e7f35d3577ddbb7004b8acbf1666783dc7aac76
 3. Reset: Sonraki değişiklikleri görebiliyorsun.   git reset 7e7f35d3577ddbb7004b8acbf1666783dc7aac76

 # *REVERT*  50:17

 - git revert 7e7f35d3577ddbb7004b8acbf1666783dc7aac76
 - ilgili versiyonun tüm geçmişini çıkarır. sen kullanıcı olarak istemediklerini temizlersin.
 - Sonrasında
 - git add .
 - git commit -m 'explanation'
 - git revert --continue

 # *STASH* 52:58

Araya farklı bir iş girdiğinde dosyaya commit yapmadan saklama şansı veriyor.
 - git stash
 - git stash list\
 - git stash apply stash@{0}

  # *GUI* 57:16

Komutlara ihtiyaç olmadan görsellerle GitHub işlevlerini yapma şansı veriyor.