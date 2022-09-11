# ProjetoFinalBagmon

## visualiza a versão do vagrant    
```
vagrant --version

``` 
## visualiza a versão do git
```
git --version
```
## configura o nome do usuario do git
```
git config --global user.name 
```
## configura o email do seu git 
```
git config --global user.email
```
* NOTA - se utilizar o global não precisara configurar novamente

## Clona um repositório em um diretório
```
git clone
```
## instala o plugin do vagrant
```
Vagrant plugin install vagrant-vbguest
```
## criar Vagrantfile
```
vagrant init GuiDev/Ubuntu-Rails5x --box-version 1.0.0

```
## Verificar Vagrantfile e modificar ela de acordo com o que esta a baixo
```
Vagrant.configure("2") do |config|
 config.vm.box = "GuiDev/Ubuntu-Rails5x"
 config.vm.box_version = "1.0.0"
 config.vm.network :forwarded_port, guest: 3000, host: 3000
 config.vm.network :forwarded_port, guest: 5432, host: 5432
 config.vm.provider "virtualbox" do |vb|
 vb.gui = true
 vb.memory = "1024"
 end
end

```
## Iniciar Vagrant  
```
vagrant up
```
## pausar o vagrant
```
vagrant suspend
```
## parar o vagrant
```
vagrant halt
```
## conectar na maquina
```
vagrant ssh
```
## verifica a versão do ruby
```
Ruby -v

```
## verifica a versão do rails
```
Rails -v 

```
## verifica aversão do postgresql
``` 
psql --version

```
## mudar o diretório atual de trabalho
```
cd ..

```
## exibe o que tem no diretorio atual
```
ls
```
## entra na pasta vagrant
```
cd vagrant
```
## pode ver os comandos disponíveis 
```
rvm list

```
## Para listar todos os rubis instaláveis ​​de RVM
```
rvm list known
```
## instala a versão do ruby
```
rvm install 2.3

```
## muda a versão do ruby
```
rvm use 2.6
```
## cria arquivo do ruby
```
ruby nome_arquivo.rb
```
## cria um novo projedo no rails
```
rails new projetinho

```
## entra na pasta do projeto
```
cd projetinho

```
## starta o projeto
```
rails server -> rails s -b 0.0.0.0
```

## cria um novo projeto no rails
```
rails new projetinho
```
## Especificando a versão do Rails a ser usada ao criar um novo aplicativo
```
rails _5.2_ new <nomedoprograma>
```
## buscar o postgres no google database.yml
``` 
rails _5.2_ new <nomedoprograma> -d postgresql
```
## cria um arquivo de modelo nome da entidade, no caso o ‘Model’ e em seguida os atributos e seus tipos
```
rails generate scaffold <Model> <campo:tipo> <campo:tipo> …
```
## Um scaffold é um conjunto de arquivos gerados automaticamente que formam a estrutura básica de um projeto Rails
```
rails g scaffold City description:string code:integer image
```

## descobre qual banco de dados você está usando
```
rails dbconsole
```
##
```
rails db

```
## pega a lista de tesk
```
rails -T

```
##
```
rails -T db

```
##
```
RAILS_ENV=production rails s -b 0.0.0.0
```
##
```
rails s -b 0.0.0.0 -e production

```
##
```
rails generate
```
