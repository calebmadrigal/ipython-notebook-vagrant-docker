ENV['VAGRANT_DEFAULT_PROVIDER'] ||= 'docker'

Vagrant.configure("2") do |config|
  config.vm.provider "docker" do |d|
    d.name = "hn-tracker"
    d.build_dir = "."
    d.remains_running = true
    # I'm not sure why, but if has_sst is true, Vagrant hangs on "vagrant up". But "vagrant ssh"
    # still works with has_ssh set to false
    d.has_ssh = false
  end
  config.ssh.insert_key = true
end
