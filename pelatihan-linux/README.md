# Fun Project Pelatihan Linux Command

1. Membuat folder dan masuk kedalamnya
  ```
mkdir artists_who_can_sing && cd artists_who_can_sing
  ```
2. Mengunduh file dari google drive
  ```
wget --no-check-certificate "https://docs.google.com/uc?export=download&id=1lV1HVmPTY_BOAK6ToXymRu7V5eVfR0ut" -O tutorials.zip
  ```
3. Extract zip ke folder singing_tutorials
  ```
unzip tutorials.zip -d singing_tutorials
  ```
4. Masuk ke folder dan menampilkan isi file dan file tersembunyi
  ```
cd singing_tutorials/ && ls -la
  ```
5. Filtering file dan append ke flag.txt di folder sebelumnya
  ```
find .*opera*NBAYoungboy* -exec grep -h 'FLAG{[^}]*}' {} + > ../flag.txt
  ```
6. Mundur direktori sebelumnya dan download binary dari link yang ada di flag sebelumnya
  ```
cd ../ && wget https://files.catbox.moe/9l4qu8 -O plsrunmeiamnotmalwarefr
  ```
7. Set permission and run
  ```
chmod +x plsrunmeiamnotmalwarefr && ./plsrunmeiamnotmalwarefr
  ```
8. Melihat proses yang berjalan
  ```
ps aux
  ```
9. Validasi stop checker dengan membuat file
  ```
touch ransom.moolah && ps aux
  ```
10. Mematikan proses program
  ```
kill <PID> && ps aux
  ```
11. Membuat user, set groups, dan login
  ```
sudo adduser yabadabadoo && sudo usermod -aG sudo yabadabadoo && groups yabadabadoo && su yabadabadoo
  ```
12. membuat folder, dan set owner dan permission
  ```
sudo mkdir fufufafa && sudo chown yabadabadoo:root fufufafa && sudo chmod 770 fufufafa && su <other_user> && cd fufufafa
  ```
13. Filtering flag di seluruh directory /var/tmp/pls_solve_this_puzzle/
  ```
grep -h -rne 0000 /var/tmp/pls_solve_this_puzzle/ | sed 's/9:000000[0-9][0-9]://g' | sed 's/0000//g' |tr -s '[:space:]'| awk '!seen[$0]++'| tr -d '[:space:]' | xxd -r -p > flag2.txt
  ```
14. Menyalin flag kedua dari artists_who_can_sing ke fufufafa 
  ```
sudo cp flag2.txt fufufafa/
  ```
15. Menghapus /var/tmp/pls_solve_this_puzzle/
  ```
sudo rm -rf /var/tmp/pls_solve_this_puzzle/
  ```
