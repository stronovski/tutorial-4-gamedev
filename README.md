# Implementasi Level Baru
## 1. Membuat Scene Level2
Scene Level2.tscn berupa Node2D dibuat agar dapat mengimplementasikan level design sesuai semestinya.

## 2. Membuat Tiles pada Level 2
Mirip seperti pembuatan tilemap pada level 1, pertama-tama TileMap akan dibuat sebagai child dari Node2D, kemudian file asset tilemap akan diimport sehingga memiliki tampilan yang sesuai. Setelah itu, tiles ditambahkan ke dalam scene untuk membuat desain dari level 2. Agar player dan objek lain dapat melakukan collision dengan tilemap, maka ditambahkan layer physics 0 yang kemudian akan di-_tweak_ dan dimodifikasi sesuai dengan kebutuhan dari tilemap tersebut. Dapat dilihat bahwa tilemap pada level 1 (mountain) berbeda dengan tilemap pada level 2, yaitu dirt.

## 3. Membuat Objek Musuh
Untuk membuat objek musuh yang baru, scene FallingBee.tscn yang memiliki root node RigidBody2D ditambahkan. Setelah itu, child node berupa Sprite2D akan ditambahkan ke root node dan texture dari sprite akan diatur menjadi bee yang terdapat di dalam asset. CollisionShape2D juga akan ditambahkan supaya objek musuh tersebut dapat melakukan collision dengan tiles. Setelah itu, AreaTrigger yang sebelumnya dibuat akan didrag ke root node, lalu Scene Name akan diganti menjadi LoseScreen agar dapat menampilkan layar ketika pemain kalah.

## 4. Meletakkan Spawner dalam Level2
Object spawner yang berupa Node2D akan diletakkan di dalam scene Level2. Selain itu, obstacle dari object spawner tersebut akan berubah dari FallingFish menjadi FallingBee agar objek musuh yang ada di level 2 berbeda dengan yang terdapat di level 1.

## 5. Menambahkan Background pada Kedua Level
Untuk menambahkan background pada kedua level, node Sprite2D ditambahkan sebagai child dari rootnode di kedua level scene tersebut. Setelah itu, texture dari sprite akan diganti menyesuaikan dengan level. Pada kasus ini, level 1 adalah level mountain, dan level 2 adalah level hutan. Setelah menambahkan background, ubah SceneName AreaTrigger yang terdapat di level2 menjadi WinScene supaya layar ketika pemain menang dapat terlihat. Setelah mengimplementasikan hal tersebut, maka game selesai diimplementasikan.

referensi:
- https://csui-game-development.github.io/tutorials/tutorial-4/
