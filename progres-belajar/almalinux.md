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
/var/lib/libvirt/images
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

masukkan command

```
firewall-cmd --list-all-zone
```

```
firewall-cmd --zone=public --remove-service =dhcpv6-client --permanent
```

**work, trusted, nm-shared, libvirt-routed, libvirt, home, internal harus kosong service nya 
untuk libvirt doang sisain sshnya aja
untuk publik sisain copit sama ssh 
drop tidak perlu di ubah
dmz tidak perlu di ubah
block tidak perlu di ubah**

#### untuk mengubah/ menghapus-nya bisa di lakukan dengan command ini

```
firewall-cmd --list-all --zone=work
```
```
firewall-cmd --list-all --zone=work --service
