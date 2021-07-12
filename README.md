# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* mkdir devise && cd devise

* rails new app -T

* rails g controller site/welcome index

* rails g controller site

* config/routes.rb:
* root to: 'site/welcome#index"

* Gemfile: 
* gem 'devise'

* bundle install

* rails g devise:install

* config\environments\development.rb: 
* config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

* rails g devise Admin

* rails g devise User

* config\initializers\devise.rb
* Descomente:
* config.scoped_views = false
* Altere para:
* config.scoped_views = true

* rails g devise:views admins

* rails g devise:views users

* rails db:migrate

* app\views\users\sessions\new.html.erb
* Altere para:
* Login User

* app\views\admins\sessions\new.html.erb
* Altere para:
* Login Admin

* rails g controller admins_backoffice/welcome index

* rails g controller users_backoffice/welcome index

* rails g controller admins_backoffice

* rails g controller users_backoffice

* app\views\layouts
* Crie os arquivos:
* admins_backoffice.html.erb
* users_backoffice.html.erb
* site.html.erb

* app\views\layouts\application.html.erb
* Abaixo de body:
* < h1>Layout Application - Padrão </ h1>

* copie para cada um dos arquivos criados, o conteúdo de: app\views\layouts\application.html.erb
* altere respectivamente em cada arquivo copiado o código:

* < h1>Layout Admins_Backoffice</ h1>
* < h1>Layout Users_Backoffice </ h1>
* < h1>Layout Site </ h1>

* app\controllers\admins_backoffice\welcome_controller.rb
* Altere para herdar de < AdminsBackofficeController

* app\controllers\users_backoffice\welcome_controller.rb
* Altere para herdar de < UsersBackofficeController

* app\controllers\site\welcome_controller.rb
* Altere para herdar de < SiteController

* app\controllers\admins_backoffice_controller.rb
* Acrescente:
* before_action :authenticate_admin!
* layout 'admins_backoffice'

* app\controllers\users_backoffice_controller.rb
* Acrescente:
* layout 'users_backoffice'

* app\controllers\site_controller.rb
* Acrescente:
* layout 'site'

* Gemfile: 
* gem 'tty-spinner'

* bundle install

* rails g task dev setup

* lib\tasks\dev.rake
* Altere conforme commit "Criando task para add usuários"

* rails dev:setup

* Altere conforme commit "Criando logoff para usuários":
* app\views\site\welcome\index.html.erb 
* config\initializers\devise.rb
* app\views\admins_backoffice\welcome\index.html.erb 
* app\views\users_backoffice\welcome\index.html.erb
* 




