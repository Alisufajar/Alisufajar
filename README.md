digraph hotel_erd {
  // Entitas
  Hotel [label="Hotel\n{hotel_id (PK)\nnama_hotel\nalamat_hotel\nbintang\nfasilitas}"]
  Kamar [label="Kamar\n{kamar_id (PK)\nnomor_kamar\ntipe_kamar\nharga_kamar\nstatus_kamar}"]
  Tamu [label="Tamu\n{tamu_id (PK)\nnama_tamu\nalamat_tamu\nnomor_telepon\nemail_tamu}"]
  Reservasi [label="Reservasi\n{reservasi_id (PK)\ntanggal_checkin\ntanggal_checkout\njumlah_orang\nstatus_reservasi}"]
  Pegawai [label="Pegawai\n{pegawai_id (PK)\nnama_pegawai\njabatan\ngaji\ntanggal_masuk}"]

  // Relasi
  Hotel -> Kamar [label="Banyak"]
  Kamar -> Tamu [label="Banyak"]
  Reservasi -> Kamar [label="Banyak"]
  Reservasi -> Tamu [label="Satu"]
  Reservasi -> Pegawai [label="Satu"]
}
