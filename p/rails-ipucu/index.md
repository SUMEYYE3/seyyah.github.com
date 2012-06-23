# Rails: İpucu

.fx: first

Nurettin Şenyer <seyyah@bil.omu.edu.tr>

http://seyyah.me

Haziran, 2012

Samsun

.qr: 150|http://seyyah.me/p/rails-ipucu

---

# Generator: Scaffold: only view

Evet sadece view üretmek istersek,

	!bash
	$ rails generate scaffold Institution --migration=false --skip

---

# Exception: ActiveRecord
## ::MultiparameterAssignmentErrors

Örnek

	!ruby
	def foo
	  ...
	rescue ActiveRecord::MultiparameterAssignmentErrors
	  flash[:error] = "Error: Collection of errors that occurred
	  		   during a mass assignment using the attributes= method."
	  redirect_to home_path
	end

Kaynak

- http://api.rubyonrails.org/classes/ActiveRecord/Base.html

---

# Rake

İpuçları,

	!bash
	$ rake -T
	$ rake routes
	$ rake db:drop
	$ rake db:create
	$ rake db:migrate
	$ rake db:seed
	$ rake db:setup 	# create + load:schema + seed
	$ rake db:reset 	# drop + setup
	$ rake db:test:prepare
