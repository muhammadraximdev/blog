# Django Blog Loyihasi

Ikki app: `user` (autentifikatsiya) va `main` (maqolalar).

## Tuzilma

```
blog_project/
├── blog_project/       # Asosiy konfiguratsiya
│   ├── settings.py
│   └── urls.py
├── user/               # Ro'yxatdan o'tish, kirish, chiqish
│   ├── views.py
│   ├── forms.py
│   ├── urls.py
│   └── templates/user/
│       ├── base.html
│       ├── login.html
│       └── register.html
├── main/               # Maqolalar (CRUD)
│   ├── models.py       # Tag, Article
│   ├── views.py
│   ├── forms.py
│   ├── urls.py
│   └── templates/main/
│       ├── base.html
│       ├── index.html
│       ├── article_detail.html
│       ├── my_articles.html
│       ├── article_edit.html
│       └── article_delete.html
└── manage.py
```

## URL manzillari

| URL | App | View |
|-----|-----|------|
| `/register/` | user | RegisterView |
| `/login/` | user | LoginView |
| `/logout/` | user | logout_view |
| `/articles/` | main | IndexView |
| `/articles/<slug>/` | main | ArticleDetailsView |
| `/my-articles/` | main | MyArticlesView |
| `/articles/<slug>/edit/` | main | ArticleEditView |
| `/articles/<slug>/delete/` | main | ArticleDeleteView |

## Ishga tushirish

```bash
pip install django
python manage.py migrate
python manage.py runserver
```
