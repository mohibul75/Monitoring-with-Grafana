<h1>Monitoring with Grafana</h1>

<h3>Grafana Intro</h3>

Grafana is a multi-paltform open source analytics and interactive visulization web application.
It provides: <br>

<ul>
	
<li>Charts</li>

<li>graphs</li>

<li>alerts</li>

</ul>

*********

<h3>Installation Process</h3>

First of all, you need to add the Grafana APT repositories in order to be able to install packages from them.

	sudo apt-get install -y apt-transport-https
	
	sudo apt-get install -y software-properties-common wget


In order to retrieve Grafana packages in a secure way, you need to add the GPG key to your trusted set of keys.

	wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -

Now that everything is configured, you can add the Grafana repositories to the custom APT repositories of your server.

	echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list

update your distribution packages.

	sudo apt-get update

To install Grafana, use the ***apt-get install*** command.

	sudo apt-get install grafana

start the grafana server
	
	sudo systemctl start grafana-server

check the status of grafana server

	sudo systemctl status grafana-server

