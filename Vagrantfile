Vagrant.configure("2") do |config|
  
  # Introduce aquí la configuración del servidor virtual
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  config.vm.synced_folder ".","/tarea_sisin"


  config.vm.provision "shell", inline: <<-SHELL

      # Instalación de los binarios de PHP, el driver mysqli y la extensión FPM para realizar peticiones de tipo RESTful
      sudo apt install -y php php-mysqli php-fpm

      # Generar archivo SQL con los registros de los diferentes Módulos Profesionales
      echo "-- Insertar datos de ejemplo en la tabla 'modulos'" > /home/vagrant/modulos.sql
    echo "INSERT INTO modulos.asignaturas(nombre, profesor, horas, salario, departamento) VALUES" >> /home/vagrant/modulos.sql
    echo "('BADAT', 'Tomas', 30, 2500.00, 'DAM')," >> /home/vagrant/modulos.sql    #SHIFT ALT CURSO ABAJO-->Duplico
    echo "('LMSGI', 'Bea', 40, 2000.00, 'DAM')," >> /home/vagrant/modulos.sql
    echo "('SISIN', 'Diego', 50, 1000.00, 'DAM')," >> /home/vagrant/modulos.sql
    echo "('PROGR', 'Diego', 10, 2400.00, 'DAM')," >> /home/vagrant/modulos.sql
    echo "('LEUP', 'Lorena', 5, 2500.00, 'DAM')" >> /home/vagrant/modulos.sql
    echo "('ENDES', 'Guillermo', 5, 2500.00, 'DAM')" >> /home/vagrant/modulos.sql

  SHELL

end
