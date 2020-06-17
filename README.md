#Commands 


g
Selamlar,
Gökkubbe altında söylenmemiş söz, yazılmamış blog konusu yoktur ama kimse hikayeyi benden dinlemedi diyip başlıyorum * üsküdara giderken . Genel amacım kendime notlar toparlamak olduğu için eşsiz bir bloga sahip olacağım Bil Geyts, Zukırberk gelip benden alacak teknolojideki güncel haberleri gibi bir iddiam olmadığını beyan ederek başlıyorum ilk yazıma.

Versiyon kontrol sistemi, backend'den fronend'e kod yazıyorum diyen herkesin kullandığı bir sistem. Herhangi bir yazı yazarken, tez hazırlarken 'SON', 'BU SON', 'SON_SON_SON', 'BU DA MI SON DEGIL' isimli dosyaları nereye koyacağınızı şaşırıyorsanız sizin de kesinlikle tanışmanız gereken bir sistem diye düşünüyorum. 

Öncelikle konfigürasyon ile işe başlayalım.
Remote repomuz hazır ise konfigürasyon yaparak başlıyoruz. GitHub, BitBucket git ile entegre çalışan depolarından bazılarıdır.

git config --global user.name "$kullanici_adi"
git config --global user.email "$mail_adresi"

Localdeki git'imize hangi depoya gidersen bu bilgileri kullan komutunu vermiş olduk. Repo olarak kullanacağımız dosyanın içerisine girdikten sonra aşağıdaki komutu çalıştırarak burayı artık bir depo olarak ilan ediyoruz/git'e bildiriyoruz.

git init // Konfigürasyon dosyalarını oluşturup klasörü bir git dosyası haline getirmek için

Bu komuttan sonra .git klasörünün altında konfigürasyon dosyaları oluşuyor. Bunlar local deponuz ve remote deponuz arasında eşitliği sağlamak, branchları logları tutmaya yarıyor.

Depomuza ilk dosyayı aşağıdaki şekilde ekliyoruz.
	git add <eklenecek_dosya_adi>	// adı belirtilen dosyayı ekle
	git add *						// klasörün içerisindeki tüm dosyaları ekle

Ben giderim commit'im kalır juniorlar beni hatırlasın diyerek yorumumuzu,açıklamamızı yazıyoruz.
	git commit -m "first commit"	// yapılan değişikliği belirtilent

Projemiz local'de ortamlara gönderilmeyi bekliyor. Uzak depomuzun adresini ekliyoruz :
	git remote add origin https://github.com/ahmetkaygisiz/tutorial_git.git // remote repoya adresini ekle

Eğer farklı bir branch oluşturmadıysanız, default olarak master branch'ı oluşturuluyor. Adresi verdikten sonra kodlarımızı depomuza gönderiyoruz.
	git push -u origin master // değişiklikleri remote repoya gönder 

Buraya kadar olan herşey çok kolay olsa da bu depoların genel amacı bir projede birden fazla kişinin çalışabilmesini sağlamak olduğu için işin içerisine insan (hele de benim gibi juniorlar) girdiğinde ortalık bir miktar karışabiliyor.

Çoklu projelerde çalışırken, çalışmaya başlamadan önce yapmanız ilk gereken şey güncel repoyu almak olmalıdır. Aksi takdirde sizden önce çalışan birisinin değişikliklerini almazsınız ve siz de yeni eklemeler yaparsanız ortaya karışıklıklar çıkar.
	git pull origin <branch_adi> // Remote repodaki değişiklikleri al
	git pull origin master 

Çalışmalarınızı tamamladınız, tam o sırada çılgın bir fikir geldi aklınıza. Dediniz ben balkon duvarını kırıp mutfağa katacağım... Git'in sunduğu avantajlardan biri de size bunu yapmadan önce farklı bir dal sunması, yani sen gel önce şurda çalış evi kirletme, güzel olursa evde de aynısını yaparız diyor. Bunun için bir branch oluşturuyoruz.
	
	git checkout -b <yeni_branch> <kaynak_Branch> 
	git checkout -b balkon_to_mutfaga master 



	git branch -a 		// show branches
	git branch -r  
	git show-branch

git log --oneline // Log history'sini göster

git reset --hard HEAD // En son yapılan değişiklikleri geri al. Commit edilmemiş
git revert --hard HEAD

git checkout <commit_id> // Daha önce yapılan bir commit'e geri dönmek için kullanılır.
						 // Burada yapılan değişiklikler ana branch'ı etkilemez ve o branch'a eklenemez.
						 //  Bu değişikliklikleri uygulamak için yeni bir branch oluşturmak gerekir.

git checkout -- dosya1.md

git branch <branch_name> <commit_id> // Yapılan değişiklikler ile yeni bir branch oluştur.

git branch -dr remove branch 

grep -lr '<<<<<<<' . | xargs git checkout --ours //  


Git REBASE 
	git rebase --continue
	git rebase --skip // bu nedir





