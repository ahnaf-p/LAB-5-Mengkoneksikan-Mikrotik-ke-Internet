# LAB-5-Mengkoneksikan-Mikrotik-ke-Internet
Selasa 12 Agustus 2025
  
![topo]()
# Konfigurasi Mikrotik ke Internet dengan IP dynamic
  1. Pasang kabel sesuai topologi diatas. **Interfaces > Interface list**
  2. Ganti nama Interface agar lebih mudah
     Ether-1-WAN (untuk mendapat internet dari ISP)
     Ether-2-LAN (untuk koneksi ke client)
![b]()
  4. Konfig DHCP Client untuk ether1, **IP > DHCP-Client > add(+) > Enabled [V] > interface=ether1-WAN > use peer dns=yes > use peer ntp=yes > add default route=yes**
     Jika sudah, pastikan statusnya **bound**
![c]()
  5. Cek koneksi mengunakan **ping** di terminal
  6. Jika berhasil, hasilnya akan reply.

#  Konfigurasi Mikrotik ke internet dengan IP static   
  1. Buat IP Address untuk ether1, **IP > Addresses > +**
     
  2. 
  3. Jika sudah, di setting IP windows di Control Panel, masukan IP secara manual, masukan IP yang masih 1 network
     IP 192.168.88.2 karna IP gatewaynya 192.168.88.1 SubMask 255.255.255.0 karna /24 dan DNS nya isi 8.8.8.8
  4. Sekarang Client bisa terhubung ke Internet

# Kesimpulan
  Dynamic routing cocok untuk awam karna client mendapat IP secara otomatis dan cocok untuk jaringan berskala besar karna tidak perlu setting IP satu-satu. Sedangkan Static Routing tidak cocok untuk jaringan berskala besar.
