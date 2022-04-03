# Git-Egitimi

## Versiyon kontrol sistemi nedir?

Esasen, zaman içinde dosyalarda yapılan değişiklikleri kaydetmemize izin veren bir sistemdir, böylece daha sonra bu dosyaların belirli sürümlerini görüntüleyebiliriz.

Bir sürüm kontrol sistemi veya VCS, insanlar ve ekipler projeler üzerinde birlikte çalıştıkça değişikliklerin geçmişini izler. Proje geliştikçe, ekipler, herhangi bir zamanda herhangi bir sürümün kurtarılabileceğinden emin olarak testler yapabilir, hataları düzeltebilir ve yeni kodlara katkıda bulunabilir. Geliştiriciler, öğrenmek için proje geçmişini inceleyebilir.
- Hangi değişiklikler yapıldı 
- Değişiklikleri kim yaptı 
- Değişiklikler ne zaman yapıldı 
- Değişikliklere neden ihtiyaç duyuldu

## Neden Git?

En son [Stack Overflow geliştirici][0] anketine göre, geliştiricilerin yüzde 70'inden fazlası Git'i kullanıyor ve bu da onu dünyanın en çok kullanılan VCS'si yapıyor. Git, ücretsiz ve açık kaynaklı bir dağıtılmış sürüm kontrol sistemidir.

Git, hem açık kaynak hem de ticari yazılım geliştirme için yaygın olarak kullanılır ve bireyler, ekipler ve işletmeler için önemli faydalar sağlar.

- Git, geliştiricilerin; değişikliklerinin, kararlarının ve herhangi bir projenin ilerleyişinin tüm zaman çizelgesini tek bir yerde görmelerini sağlar. Geliştiriler, bir projenin geçmişine eriştikleri andan itibaren, onu anlamak ve katkıda bulunmaya başlamak için ihtiyaç duydukları tüm içeriğe sahiptir.
- Geliştiriciler her saat diliminde çalışır. Git gibi bir [DVCS][1] ile kaynak kodu bütünlüğünü korurken işbirliği her zaman gerçekleşebilir. Geliştiriciler, dalları kullanarak üretim kodunda güvenli bir şekilde değişiklik önerebilir.
- Git'i kullanan işletmeler, ekipler arasındaki iletişim engellerini ortadan kaldırabilir ve onların en iyi işlerini yapmaya odaklanmalarını sağlayabilir. Ayrıca Git, büyük projelerde işbirliği yapmak için bir işletmedeki uzmanların hizalanmasını mümkün kılar.

<p align="center">
  <img src="https://user-images.githubusercontent.com/58858983/161418452-434fd705-2cda-4d0b-9f9d-d5fa6e016692.png">
  <h4 align="center">Resim 1 Git</h4>
</p>
<br>

## Repository Nedir?
Bir repository veya Git projesi; her dosyanın revizyon geçmişiyle birlikte, bir projeyle ilişkili tüm dosya ve klasör koleksiyonunu kapsar. Dosya geçmişi, commit adı verilen zamanda anlık görüntüler olarak görünür ve commitler, bağlantılı bir liste ilişkisi olarak bulunur ve branch(dal) adı verilen birden çok geliştirme satırında düzenlenebilir. Git bir DVCS olduğundan, repositoryler bağımsız birimlerdir ve repositorynin bir kopyasına sahip olan herkes tüm kod tabanına ve geçmişine erişebilir. Komut satırını veya diğer kullanımı kolay arayüzleri kullanarak, git repositorysinin şu özelliklerini de kullanabiliriz: geçmişle etkileşim, klonlama(cloning), branchler oluşturma, commitleme, birleştirme(merging), kod sürümlerindeki değişiklikleri karşılaştırma ve daha fazlası.

## Temel Git komutları
Git'i kullanmak için geliştiriciler, kodu kopyalamak, oluşturmak, değiştirmek ve birleştirmek için belirli komutlar kullanır. Bu komutlar doğrudan komut satırından veya GitHub Desktop veya Git Kraken gibi bir uygulama kullanılarak yürütülebilir. Git'i kullanmak için bazı yaygın komutlar şunlardır:

- git init : Yepyeni bir Git deposu başlatır ve mevcut bir dizini izlemeye başlar. Sürüm kontrolü için gerekli dahili veri yapısını barındıran mevcut dizine gizli bir alt klasör ekler.
- git clone : zaten uzaktan var olan bir projenin yerel bir kopyasını oluşturur. Klon, tüm projenin dosyalarını, geçmişini ve branchlerini içerir.
- git add : Git, bir geliştiricinin kod tabanındaki değişiklikleri izler, ancak bunları proje geçmişine dahil etmek için değişikliklerin sahnelenmesi ve anlık görüntüsünün alınması gerekir. Bu komut, iki adımlı sürecin ilk kısmı olan evrelemeyi gerçekleştirir. Aşamalı olan herhangi bir değişiklik, bir sonraki anlık görüntünün ve proje tarihinin bir parçası olacaktır. Ayrı ayrı hazırlama(Staging) ve taahhüt etme(committing), geliştiricilere kodlama ve çalışma biçimlerini değiştirmeden projelerinin geçmişi üzerinde tam kontrol sağlar.
- git commit : Anlık görüntüyü proje geçmişine kaydeder ve değişiklik izleme sürecini tamamlar. Kısacası, bir commit, fotoğraf çekmek gibi işlev görür. "git add" ile sahnelenen her şey, "git commit" ile anlık görüntünün bir parçası olacak.
- git status : Değişikliklerin durumunu; izlenmemiş, değiştirilmiş veya aşamalı olarak gösterir.
- git branch : Yerel olarak üzerinde çalışılan branchleri(dalları) gösterir.
- git merge : Geliştirme hatlarını birleştirir. Bu komut genellikle iki farklı branchte(dalda) yapılan değişiklikleri birleştirmek için kullanılır. Örneğin, bir geliştirici, dağıtım için bir feature branchinden master branchine yapılan değişiklikleri birleştirmek istediğinde bu komutu kullanır.
- git pull : Yerel geliştirme hattını, uzak meslektaşından gelen güncellemelerle günceller. Geliştiriciler, bir takım arkadaşı uzaktan o branche commit işlemi gerçekleştirirse ve bu değişiklikleri kendi yerel ortamına(kendi branchine) yansıtmak istiyorsa bu komutu kullanır.
- git push : Uzak repositoryi yerel olarak bir branchde yapılan commitlerle günceller.

<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/58858983/161419539-f6ff58b7-99cf-4124-b88a-830c785abfbd.png">
  <h4 align="center">Resim 2 Git Komutları</h4>
</p>
<br>

## GitHub Akışı
GitHub akışı, dünyanın dört bir yanındaki ekipler tarafından kullanılan temel Git komutları etrafında oluşturulmuş hafif, branch tabanlı bir iş akışıdır.

GitHub akışının altı adımı vardır, uygulandığında her birinin farklı faydaları vardır:

1. Create a Branch:  Kurallı dağıtım branchinden (genellikle master) oluşturulan konu branchleri, ekiplerin birçok paralel çabaya katkıda bulunmasına olanak tanır. Özellikle kısa ömürlü konu branchleri, ekiplerin odaklanmasını sağlar ve hızlı gönderilerle sonuçlanır.
2. Add Commits: Bir branch içindeki geliştirme çabalarının anlık görüntüleri, proje geçmişinde güvenli, geri döndürülebilir noktalar oluşturur.
3. Open a Pull Request: Bir projenin devam eden çabalarını duyurur ve şeffaf bir geliştirme sürecinin tonunu belirler.
4. Discuss and Review Code: Ekipler, kod incelemelerine şu şekilde katılır: commenting(yorumlama), testing(test etme) ve açık pr'ları(pull requests) gözden geçirme.  Kod incelemesi, açık ve katılımcı bir kültürün merkezinde yer alır.
5. Merge: Merge'e tıkladıktan sonra GitHub, yerel bir "git merge" işleminin eşdeğerini otomatik olarak gerçekleştirir. GitHub ayrıca tüm branch geliştirme geçmişini birleştirilmiş çekme isteğinde(merged pull request) tutar.
6. Deploy: Ekipler en iyi yayın döngülerini seçebilir veya sürekli entegrasyon araçlarını dahil edebilir ve deploymant branchindeki kodun sağlam bir iş akışından geçtiği güvencesiyle çalışabilir.

<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/58858983/161420029-265ecef2-e5cd-4e49-9853-fc738cbd0458.png">
  <h4 align="center">Resim 3 GitHub Akışı</h4>
</p>
<br>


## Fork (Çatallamak)
GitHub hesabınıza bir repository kopyalamanın yollarından biri, GitHub'ın web sitesinde bulunan forku kullanmaktır. Bir repositoryi forklamak, esasen bu projeyi çevrimiçi GitHub hesabınıza kopyalar. Ancak, o proje üzerinde yerel bilgisayarınızda çalışmak için projeyi klonlamalısınız.

<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/58858983/161420121-d6230aaa-57e4-46e8-8ccd-9f51b472be67.png">
  <h4 align="center">Resim 4 GitHub Fork</h4>
</p>
<br>


## Kaynaklar
- https://medium.com/swlh/an-introduction-to-git-and-github-22ecb4cb1256
- [Resim 1][3]
- [Resim 2][4]
- [Resim 3][5]
- [Resim 4][6]

[0]: https://insights.stackoverflow.com/survey/2017#technology
[1]: https://en.wikipedia.org/wiki/Distributed_version_control
[3]: https://www.hostinger.web.tr/rehberler/github-kullanimi-basit-git-komutlari
[4]: https://www.reddit.com/r/github/comments/gf27aa/git_commands_hope_it_helps_you_source_igmlindia/
[5]: https://gaboesquivel.com/blog/2018/recommendations-to-enhance-your-github-flow/
[6]: https://medium.com/swlh/an-introduction-to-git-and-github-22ecb4cb1256
