
# Django Müsahibə Sual və Cavabları

Bu repozitoriyada Django ilə bağlı müsahibə sual-cavabları toplanılır. Siz də bu repozitoriyaya əlavələr edə bilərsiniz. Əlavələriniz üçün pull request göndərə bilərsiniz.

### İçindəkilər

--------------------

1. [Django nədir və nə üçün istifadə olunur?](#django-n%C9%99dir-v%C9%99-n%C9%99-%C3%BC%C3%A7%C3%BCn-istifad%C9%99-olunur)
2. [Model-View-Controller (MVC) memarlıq şablonu Django'da necə işləyir?](#model-view-controller-mvc-memarl%C4%B1q-%C5%9Fablonu-django-da-nec%C9%99-i%C5%9Fl%C9%99yir)
3. [Django proyekti necə yaradılır?](#django-proyekti-nec%C9%99-yarad%C4%B1l%C4%B1r)
4. [Django app-lərinin məqsədi nədir?](#django-app-l%C9%99rinin-m%C9%99qs%C9%99di-n%C9%99dir)
5. [Django app-ləri necə yaradılır?](#django-app-l%C9%99ri-nec%C9%99-yarad%C4%B1l%C4%B1r)
6. [Django'da modellər necə təyin edilir və migrasiyalar nə üçün istifadə olunur?](#django-da-modell%C9%99r-nec%C9%99-t%C9%99yin-edilir-v%C9%99-migrasiyalar-n%C9%99-%C3%BC%C3%A7%C3%BCn-istifad%C9%99-olunur)
7. [Django'da şablonların (templates) rolu necədir?](#django-da-%C5%9Fablonlar%C4%B1n-templates-rolu-nec%C9%99dir)
8. [Django URL yönləndirməsini necə həll edir?](#django-url-y%C3%B6nl%C9%99ndirm%C9%99sini-nec%C9%99-h%C9%99ll-edir)
9. [Django admin saytı nədir və onunla bir modeli necə qeydiyyatdan keçirə bilərsiniz?](#django-admin-sayt%C4%B1-n%C9%99dir-v%C9%99-onunla-bir-modeli-nec%C9%99-qeydiyyatdan-ke%C3%A7ir%C9%99-bil%C9%99rsiniz)
10. [Django'da QuerySet nədir və o, sadə SQL sorğusundan necə fərqlənir?](#django-da-queryset-n%C9%99dir-v%C9%99-o-sad%C9%99-sql-sor%C4%9Fusundan-nec%C9%99-f%C9%99rql%C9%99nir)
11. [Django ORM-i (Object-Relational Mapping) istifadə edərək verilənlər bazasından məlumatları necə əldə edə olunur?](#django-orm-i-object-relational-mapping-istifad%C9%99-ed%C9%99r%C9%99k-veril%C9%99nl%C9%99r-bazas%C4%B1ndan-m%C9%99lumatlar%C4%B1-nec%C9%99-%C9%99ld%C9%99-ed%C9%99-olunur)
12. [Django-nun kontekst prosessorlarının məqsədini izah edin.](#django-nun-kontekst-prosessorlar%C4%B1n%C4%B1n-m%C9%99qs%C9%99dini-izah-edin)
13. [Django'da datalar view-lardan template-lərə necə ötürülür?](#django-da-datalar-view-lardan-template-l%C9%99r%C9%99-nec%C9%99-%C3%B6t%C3%BCr%C3%BCl%C3%BCr)
14. [Django'nun built-in istifadəçi autentifikasiya sistemi nədir?](#django-nun-built-in-istifad%C9%99%C3%A7i-autentifikasiya-sistemi-n%C9%99dir)


--------------------

### Django nədir və nə üçün istifadə olunur?

Django, Python proqramlaşdırma dilində yazılmış açıq mənbəli bir veb framework-dür. Django, veb saytların və veb tətbiqlərinin yaradılması üçün istifadə olunur. Django, veb saytların yaradılması üçün lazım olan müxtəlif funksionallıqları təmin edir. 

Django-nun əsas funksionallıqları aşağıdakılardır:

- ORM (Object-Relational Mapping) sistemi
- Şablon sistemləri
- Formlar
- İstifadəçi autentifikasiyası
- Admin panel
- URL yönləndirməsi
- Middleware
- Sessionlar
- Cache
- Security


### Model-View-Controller (MVC) memarlıq şablonu Django'da necə işləyir?

Django, Model-View-Template (MVT) memarlıq şablonunu istifadə edir. Bu memarlıq şablonunda Model, View və Template komponentləri yer alır.

- Model: Model, verilənlər bazasında məlumatların saxlanılması və əməliyyatların aparılması üçün lazımlıdır. Django-da model, verilənlər bazasında cədvəl kimi təmsil olunur. Django ORM-i vasitəsilə model obyektləri ilə verilənlər bazasında əməliyyatlar aparılabilir.
- View: View, istifadəçi tərəfindən göstərilən məlumatların hazırlanması üçün lazımlıdır. View, modeldən məlumatları alır və template-lərə ötürür. View, template-lərə məlumatların ötürülməsindən məsuldur.
- Template: Template, istifadəçiyə məlumatların göstərilməsi üçün lazımlıdır. Template, HTML və Django template dildə yazılır. Template, view-dan alınan məlumatları göstərmək üçün istifadə olunur.

Bu memarlıq şablonunda Controller komponenti yoxdur. Django-da Controller funksionallığı View komponenti ilə əvəz olunur.


### Django proyekti necə yaradılır?

Django proyekti yaratmaq üçün aşağıdakı komandaları işə salmaq lazımdır:

```bash
django-admin startproject myproject
```

Bu komanda işə salındıqdan sonra `myproject` adlı yeni bir Django proyekti yaradılır. Bu proyektin daxilində aşağıdakı fayllar yer alır:

- `manage.py`: Django proyektini idarə etmək üçün lazımlıdır.
- `myproject/`: Django proyektinin fayllarının yer aldığı qovluqdur.
- `myproject/__init__.py`: Python paketi olduğunu bildirir.
- `myproject/settings.py`: Django proyektinin ayarlarının yer aldığı fayldır.
- `myproject/urls.py`: Django proyektinin URL konfiqurasiyasının yer aldığı fayldır.
- `myproject/asgi.py`: ASGI protokolunu istifadə edən serverlər üçün ASGI konfiqurasiyasının yer aldığı fayldır.
- `myproject/wsgi.py`: WSGI protokolunu istifadə edən serverlər üçün WSGI konfiqurasiyasının yer aldığı fayldır.


### Django app-lərinin məqsədi nədir?

Django app-ləri, Django proyektində müxtəlif funksionallıqları təmin etmək üçün istifadə olunur. Django app-ləri, Django proyektini daha modullu və daha təşkilatlı hala gətirir. Hər bir Django app-i müstəqil funksionallıqları təmin edir və proyektin daha yaxşı təşkil olunmasına kömək edir.


### Django app-ləri necə yaradılır?

Django app-ləri yaratmaq üçün aşağıdakı komandaları işə salmaq lazımdır:

```bash
python manage.py startapp myapp
```

Bu komanda işə salındıqdan sonra `myapp` adlı yeni bir Django app-i yaradılır. Bu app-in daxilində aşağıdakı fayllar yer alır:

- `models.py`: Model obyektlərinin təyin edildiyi fayldır.
- `views.py`: View funksionallıqlarının təyin edildiyi fayldır.
- `urls.py`: URL konfiqurasiyasının təyin edildiyi fayldır.
- `admin.py`: Admin panel üçün model obyektlərinin qeydiyyatdan keçirilməsi üçün lazımlıdır.
- `apps.py`: App-in konfiqurasiyasının təyin edildiyi fayldır.
- `tests.py`: Testlərin təyin edildiyi fayldır.


### Django'da modellər necə təyin edilir və migrasiyalar nə üçün istifadə olunur?

Django-da model obyektləri təyin etmək üçün `models.py` faylında model obyektləri yaradılır. Model obyektləri, verilənlər bazasında cədvəl kimi təmsil olunur. Model obyektləri təyin edildikdən sonra migrasiyaların yaradılması üçün aşağıdakı komandalar işə salınır:

```bash
python manage.py makemigrations
python manage.py migrate
```

`makemigrations` komandası, model obyektlərində dəyişikliklər olduğu təqdirdə migrasiyaların yaradılmasını təmin edir. `migrate` komandası, migrasiyaların verilənlər bazasına tətbiq edilməsini təmin edir.


### Django'da şablonların (templates) rolu necədir?

Django-da şablonlar, istifadəçiyə məlumatların göstərilməsi üçün lazımlıdır. Şablonlar, HTML və Django template dildə yazılır. View funksionallığından alınan məlumatlar şablonlara ötürülür və istifadəçiyə göstərilmək üçün hazırlanır. Şablonlar, proyektin `templates` qovluğunda yer alır.


### Django URL yönləndirməsini necə həll edir?

Django-da URL yönləndirməsini həll etmək üçün `urls.py` faylında URL konfiqurasiyası təyin olunur. Bu faylda URL pattern-ləri təyin olunur və hər bir URL pattern-i bir view funksiyasına yönləndirilir. Django, URL pattern-ləri yoxlayır və uyğun gələn URL pattern-i tapdıqda həmin view funksiyasını işə salır.


### Django admin saytı nədir və onunla bir modeli necə qeydiyyatdan keçirə bilərsiniz?

Django admin saytı, Django admin panel vasitəsilə verilənlər bazasındakı məlumatları idarə etmək üçün lazımlıdır. Django admin saytı, model obyektlərinin admin panelində göstərilməsini və idarə edilməsini təmin edir. Bir modeli admin panelində qeydiyyatdan keçirmək üçün aşağıdakı addımaları izləmək lazımdır:

1. `admin.py` faylında model obyektini import etmək.
2. Model obyektini `admin.site.register()` funksiyası ilə qeydiyyatdan keçirmək.


### Django'da QuerySet nədir və o, sadə SQL sorğusundan necə fərqlənir?

Django-da QuerySet, verilənlər bazasından məlumatların əldə edilməsi üçün lazımlıdır. QuerySet, verilənlər bazasından məlumatların seçilməsi, filtrə edilməsi, sıralanması və s. üçün istifadə olunur. QuerySet, SQL sorğularından fərqli olaraq, Python dildə yazılır və Django ORM-i vasitəsilə verilənlər bazasına çevrilir.


### Django ORM-i (Object-Relational Mapping) istifadə edərək verilənlər bazasından məlumatları necə əldə edə olunur?

Django ORM-i vasitəsilə verilənlər bazasından məlumatları əldə etmək üçün aşağıdakı addımaları izləmək lazımdır:

1. Model obyektini import etmək.
2. Model obyektindən QuerySet yaratmaq.
3. QuerySet-də filtrələr əlavə etmək.
4. QuerySet-də sıralama əlavə etmək.
5. QuerySet-də limit və offset təyin etmək.
6. QuerySet-də digər əməliyyatlar aparılması.


### Django-nun kontekst prosessorlarının məqsədini izah edin.

Django'nun kontekst prosessorları, Django veb tətbiqetməsində istifadə olunan hər bir şablonun kontekstində əlavə məlumat əlavə etmək məqsədini xidmət edir. Şablonun konteksti, o şablonun istifadə üçün mövcud olan dəyişənlər və məlumatlara istinad edir. Kontekst prosessorları, bu kontekstinə tərzində istənilən məlumatı global olaraq əlavə etməyə imkan verir.

Kontekst prosessorları istifadə etmək, şablonlarınızı DRY (Don't Repeat Yourself - Özünü Təkrar Etmə) prinsiplərinə uyğunlaşdırmağa kömək edir. Məsələn, hər bir şablonun kontekstində mövcud olan bir məlumatı, kontekst prosessorları vasitəsilə bütün şablonlarda əlavə etmək olar.


### Django'da datalar view-lardan template-lərə necə ötürülür?

Django-da datalar view-lardan template-lərə ötürülməsi üçün `render()` funksiyası istifadə olunur. Bu funksiya, view-dan template-ə məlumatların ötürülməsini təmin edir. `render()` funksiyasının sintaksisi aşağıdakı kimidir:

```python
from django.shortcuts import render

def my_view(request):
    data = {'name': 'John Doe'}
    return render(request, 'my_template.html', data)
```

Bu kod nümunəsində `render()` funksiyası, `my_template.html` adlı template-ə `data` adlı məlumatları ötürür.


### Django'nun built-in istifadəçi autentifikasiya sistemi nədir?

Django, built-in istifadəçi autentifikasiya sistemi təmin edir. Bu autentifikasiya sistemi, istifadəçilərin qeydiyyatdan keçməsini, daxil olmağını və şifrələrini dəyişməsini təmin edir. Django built-in autentifikasiya sistemi, istifadəçilərin autentifikasiya proseslərini idarə etmək üçün lazımlıdır. Bu sistemi istifadə etmək üçün aşağıdakı addımaları izləmək lazımdır:

1. `urls.py` faylında autentifikasiya URL-lərini təyin etmək.
2. `settings.py` faylında autentifikasiya ayarlarını təyin etmək.
3. `views.py` faylında autentifikasiya funksionallıqlarını təyin etmək.
4. `forms.py` faylında autentifikasiya formalarını təyin etmək.
5. `templates` qovluğunda autentifikasiya template-lərini yaratmaq.