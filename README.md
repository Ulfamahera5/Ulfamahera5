<?php
include('koneksi.php');
if(isset($_POST['tambah'])){
    $Id_buku=$_POST['id_buku'];
    $Judul_buku=$_POST['judul_buku'];
    $Nama_pengarang=$_POST['nama_pengarang'];
    $Nama_penerbit=$_POST['nama_penerbit'];
    $Tahun_terbit=$_POST['tahun_terbit'];
    $Harga_buku=$_POST['harga_buku'];
}
$hasilinsert= mysqli_query($conn,"INSERT INTO buku (id_buku,judul_buku,nama_pengarang,nama_penerbit,tahun_terbit,harga_buku) 
                                            VALUES ('$id_buku','$judul_buku','$nama_pengarang','$nama_penerbit','$tahun_terbit','$harga_buku')");

if(!$hasilinsert){
    echo "gagal";
}

else{
    header('index.php');
}
}
?>
