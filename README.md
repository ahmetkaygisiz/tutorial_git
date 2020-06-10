#Commands 


git init // Konfigürasyon dosyalarını oluşturup klasörü bir git dosyası haline getirmek için

git add * 						// Bulunan klasördeki tüm dosyaları ekle
git add <eklenecek_dosya_adi>	// adı belirtilen dosyayı ekle

git commit -m "first commit"	// yapılan değişikliği belirt

git remote add origin https://github.com/ahmetkaygisiz/tutorial_git.git // remote repoya adresini ekle

git push -u origin master // değişiklikleri remote repoya gönder 

git branch -a 		// show branches
git branch -r  
git show-branch

git log --oneline // Log history'sini göster

git revert HEAD // En son yapılan değişiklikleri geri al.

git checkout <commit_id> // Daha önce yapılan bir commit'e geri dönmek için kullanılır.
						 // Burada yapılan değişiklikler ana branch'ı etkilemez ve o branch'a eklenemez.
						 //  Bu değişikliklikleri uygulamak için yeni bir branch oluşturmak gerekir.

git branch <branch_name> <commit_id> // Yapılan değişiklikler ile yeni bir branch oluştur.


<<<<<<< HEAD
=======

git reset <commit_id> // 
>>>>>>> git reset
