**Pastikan menggunakan flashdisk yang sudah di isi iso almalinux**

pilih bahasa english dan keyboard english

pilih instalation destination: 
pencet yang 1tb sampai ceklis (sesuaikan dengan storage)
lalu storage configuration, custom, done


encryp my data

click here to create them automaticly

**BAGIAN PARTISI** (SESUAKAN DENGAN KAPASITAS STORAGE)
contoh:

/home 5gb
/20 gb
/boot (tidak perlu di ubah)
/boot/efi (tidak perlu di ubah)
swap 8gb

pencet tanda +
mount point: /var/log
desire capacity:5 gb

pencet tanda +
/var/lib/libvirt
desire capacity masukkan sisa avaible space (GB)

pencet (clik here apa gitu) di kanan atas

buat password
accept changes

KDUMP
disable

software selection
pilih virtualization host: security tools, headless managemnt, virtualization platform

root account 
disable


user creation

buat nama user
buat password user

done2x

reboot system
masukkan password 
masukkan nama user
masukkan password user

sudo su
```
systemctl enable firewalld
```
```
systemctl start firewalld
```

pastikan firewall sudah berjalan, untuk memastikanya masukkan command
```
systemctl status firewalld
```
