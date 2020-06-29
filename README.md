Django处理请求的步骤:
1. request中有没有`urlconf`属性(`HttpRequest.urlconf`)?  
&nbsp;&nbsp;- 有: 使用指定的`urlconf`  
&nbsp;&nbsp;- 无: 使用settings.py中的`ROOT_URLCONF`  
2. 导入`urlconf`中的`urlpatterns`变量  
&nbsp;&nbsp;- `urlpatterns`通常是个`list`  
&nbsp;&nbsp;- `urlpatterns`中的元素类型是django的`path`或`re_path`    
3. 遍历`urlpatterns`, 逐个匹配URL  
&nbsp;&nbsp;- 请求的url存放在`HttpRequest.path_info`属性中  
&nbsp;&nbsp;- 匹配到之后即停止遍历  
4. 匹配成功后, Django会调用相应的视图(view)来处理请求, 两种数据会传递给view:  
&nbsp;&nbsp;① `HttpRequest`实例  
&nbsp;&nbsp;② 在`path`或`re_path`中捕获到的参数, 包括有名字的和没名字的  
5. 如果第3步没有匹配到, 或第4步抛出了异常, Django会调用特定的视图(views), 这些视图专门用于处理异常

```python
# views.py
def year_archive(request, num):
    return JsonResponse({
            'articles': serialize('python', Article.objects.filter(pub_date__year=num))
        })
def month_archive(request, year=2020, month=7):
        return JsonResponse({
            'articles': serialize('python', Article.objects.filter(pub_date__year=year, pub_date__month=month))
        })
# urls.py
urlpatterns = [
    path('articles/2003/', views.special_case_2003),
    # 会给view传递一个位置参数(Positional Argument)
    re_path(r'^articles/([0-9]{4})/$', views.year_archive),
    # 会给view传递两个关键字参数(Keyword Argument)
    path('articles/<int:year>/<int:month>/', views.month_archive),
    path('articles/<int:year>/<int:month>/<slug:slug>/', views.article_detail),
]
```

- 使用`<>`来捕获url中的值, 默认数据类型为`str`
- 可以转化捕获到的值的类型, 例如`<int:month>`可以将字符串`'12'`变成数字`12`
- `/`不会被捕获进参数
- url首位不需要加`/`
- `/articles/2003`将匹配不到任何`urlpatterns`, 因为缺少结尾`/`