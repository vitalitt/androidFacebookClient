# androidFacebookClient
( P.S. This is a laboratory work at the university, I do not want to delete it, so as not to forget how much I hate it)


details:
Я использовал android facebook sdk (https://developers.facebook.com/docs/android/componentsdks), 
а также модуль picasso для загрузки картинки профиля пользователя с урла.

Я зарегистрировал приложение через панель разработчика фейсбук (https://developers.facebook.com/apps/) и в файле res/values/strings.xml 
прописал id приложения для авторизации

Весь функционал лежит в классе MainActivity

onCreate - метод жизненного цикла,в нем мы получаем доступ к элементам пользовательского интерфейса(txtBirthday и т д), вешаем на кнопку авторизации коллбэк и обрабатываем его
в FacebookCallback.onSuccess(), после чего получаем response (в onCompleted) и передаем его в метод getData

getData - метод в котором мы получаем аватар пользователя с помощью graph facebook API и парсим его с помощью Picasso. Заполняем поля полученными данными.

printKeyHash - метод для получения хэш-ключа для аутентификации приложения в facebook

onActivityResult - метод обратного вызова, коллбэк, для получения активностей.

В файле AndroidManifest.xml я подключил разрешение на интернет "android.permission.INTERNET"
