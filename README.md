
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="">
<meta name="author" content="PUSDATIN PNJ">
<title>Beranda - PUSDATIN PNJ</title>
<meta http-equiv="refresh"
	content="75" />
<link rel="shortcut icon"
	href="http://152.118.191.12/public/images/favicon.ico" />
<!-- css -->
<link href="http://152.118.191.12/public/bs/css/bootstrap.min.css"
	rel="stylesheet">
<link href="http://152.118.191.12/public/bs/css/font-awesome.min.css"
	rel="stylesheet">
<link
	href="http://152.118.191.12/public/bs/css/ie10-viewport-bug-workaround.css"
	rel="stylesheet">
<link rel="stylesheet" type="text/css"
	href="http://152.118.191.12/public/css/stylebs.css" />
<link rel="stylesheet" type="text/css"
	href="http://152.118.191.12/chat/css/chat.css" />

<script src="http://152.118.191.12/public/js/jquery-1.11.3.min.js"
	type="text/javascript"></script>

<script src="http://152.118.191.12/public/bs/js/bootstrap.min.js"
	type="text/javascript"></script>

<script type="text/javascript"> 
    var GB_ROOT_DIR = "http://152.118.191.12/public/greybox/";
</script>

<script type="text/javascript"
	src="http://152.118.191.12/public/greybox/AJS.js"></script>
<script type="text/javascript"
	src="http://152.118.191.12/public/greybox/AJS_fx.js"></script>
<script type="text/javascript"
	src="http://152.118.191.12/public/greybox/gb_scripts.js"></script>
<link href="http://152.118.191.12/public/greybox/gb_styles.css"
	rel="stylesheet" type="text/css" />

<script type="text/javascript">
GB_myShow = function(caption, url, height, width, is_reload_on_close) {
	var options = {
		caption: caption,
		height: height || 500,
		width: width || 500,
		fullscreen: false,
		overlay_click_close: true,
		show_loading: true,
		reload_on_close: is_reload_on_close || false
	}
	var
	win = new GB_Window(options);
	return win.show(url);
}
var count=1;
jQuery(document).ready(function() {
	refresh();
    window.callback = function(data){
        //count++;
        //console.log(data,count );
    	$('p[id=status_ip]').text(data.ip);
        $('p[id=status_durasi]').text(data.uptime);
        $('p[id=status_download]').text(formatBytes(data.bytes_out));
        $('p[id=status_upload]').text(formatBytes(data.bytes_in));
    };

    //Loop every 2 seconds
    var tid = setInterval(refresh, 1000);
    function refresh(){
        $.getScript("http://hotspot.pnj.ac.id/status", function(data){});
        $.get("http://152.118.191.12/index.php/user/cek_login", function(data){});
    };

    function formatBytes(bytes,decimals) {
 	   if(bytes == 0) return '0 Byte';
 	   var k = 1000;
 	   var dm = decimals + 1 || 3;
 	   var sizes = ['Bytes', 'KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'];
 	   var i = Math.floor(Math.log(bytes) / Math.log(k));
 	   return (bytes / Math.pow(k, i)).toPrecision(dm) + ' ' + sizes[i];
 	}
});
(function($){
    $(document).ready(function(){
        $('ul.dropdown-menu [data-toggle=dropdown]').on('click', function(event) {
  			event.preventDefault(); 
  			event.stopPropagation(); 
  			$(this).parent().siblings().removeClass('open');
  			$(this).parent().toggleClass('open');
  		});
  	});
})(jQuery);

</script>

</head>
<body>
	<!-- Jika Javascript tidak diaktifkan -->
	<noscript>
		<style type="text/css">
#container-fluid {
	display: none
}
</style>
		<p>Perangkat Anda tidak mendukung Javascript atau tidak diaktifkan.
			Mohon aktifkan(enable) Javacript pada browser Anda.</p>
	</noscript>
    <nav class="navbar navbar-inverse navbar-fixed-top">
	<div class="container-fluid menu_atas">
		<div class="navbar-header">
			<button type="button" class="navbar-toggle collapsed"
				data-toggle="collapse" data-target="#navbar">
				<span class="sr-only">Toggle navigation</span> <span
					class="icon-bar"></span> <span class="icon-bar"></span> <span
					class="icon-bar"></span>
			</button>
			<a href="http://hotspot.pnj.ac.id/alogin" class="navbar-brand"><i
				class="fa fa-home"></i> Beranda</a>
		</div>
		<div id="navbar" class="navbar-collapse collapse">
			<ul class="nav navbar-nav">
                        <li class="dropdown"><a href="#" class="dropdown-toggle"
					data-toggle="dropdown"><i class="fa fa-user"></i> Profile <span
						class="caret"></span></a>
                            <ul class="dropdown-menu">
						<li><a href="http://152.118.191.12/index.php/user"><i class="fa fa-user"></i>
								My Profile</a></li>
					    						<li><a href="http://152.118.191.12/index.php/user/edit_profil"><i
								class="fa fa-pencil-square-o"></i> Edit Profile</a></li>
											</ul>
                          </li>
				<li><a href="http://152.118.191.12/index.php/user/berita/4"><i
						class="fa fa-question-circle"></i> F.A.Q</a></li>
              <li class="dropdown"><a href="#" class="dropdown-toggle"
					data-toggle="dropdown" role="button" aria-haspopup="true"
					aria-expanded="false"><i class="fa fa-tasks"></i> Yang Online <span
						class="label label-danger">365</span><span
						class="caret"></span></a>
					<ul class="dropdown-menu">
						<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=8">Administrasi Niaga <span class="label label-info">14</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=7">Akuntansi <span class="label label-primary">26</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=20">Gedung Alat Berat <span class="label label-success">3</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=3">Gedung Direktorat Lt.1 <span class="label label-success">6</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=1">Gedung Direktorat Lt.2 <span class="label label-info">17</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=21">Gedung Direktorat Ruang Keuangan <span class="label label-success">8</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=22">Gedung Kearsipan <span class="label label-success">6</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=15">Gedung Serba Guna (GSG) Lt.1 <span class="label label-success">5</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=10">Gedung Serba Guna (GSG) Lt.2 <span class="label label-info">13</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=17">PUSDATIN <span class="label label-success">5</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=6">Teknik Elektro <span class="label label-info">14</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=14">Teknik Grafika & Penerbitan <span class="label label-success">4</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=18">Teknik Infromatika & Komputer <span class="label label-primary">26</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=5">Teknik Mesin <span class="label label-info">14</span></a></li>
												<li><a
							href="http://152.118.191.12/index.php/user/online?lokasi=4">Teknik Sipil <span class="label label-primary">25</span></a></li>
											</ul></li>
				<li><a href="http://152.118.191.12/index.php/user/statistik_sebulan"><i
						class="fa fa-line-chart"></i> Statistik</a></li>
				<li><a href="http://152.118.191.12/index.php/user/download"><i
						class="fa fa-cloud-download"></i> Download</a></li>
				<li><a href="http://hotspot.pnj.ac.id/logout"><i
						class="fa fa-sign-out"></i> <b>Logout</b></a></li>
			</ul>
		</div>
		<!--/.nav-collapse -->
	</div>
</nav>    <br>
	<div class="container-fluid">
		<div class="row">
			<div class="col-sm-3 col-md-2 sidebar">
<img alt="Foto Profil" class="img-responsive center-block" src="http://152.118.191.12/upload/foto_profil/2016_09_07_1473222409_9942.jpg" />

<ul class="nav">
		<li><a href="http://152.118.191.12/index.php/user/ubah_foto_profil"
		onclick="return GB_myShow('Upload Foto', this.href, 600,700, true)"
		title="Upload Foto">Ubah Foto Profil</a></li>
	<li><a href="http://152.118.191.12/index.php/user/ubah_password"
		onclick="return GB_myShow('Ubah Password', this.href, 600,700, true)"
		title="Ubah Password">Ubah Password</a></li>
	</ul><hr>
<i class="fa fa-map-marker"></i> <b>IP Address</b>
<p id="status_ip" class="text-muted">-</p>
<i class="fa fa-clock-o"></i> <b>Durasi Koneksi</b>
<p id="status_durasi" class="text-muted">-</p>
<i class="fa fa-download"></i> <b>Paket Terdownload</b>
<p id="status_download" class="text-muted">-</p>
<i class="fa fa-upload"></i> <b>Paket Terupload</b>
<p id="status_upload" class="text-muted">-</p></div>    		<div
				class="col-sm-9 col-sm-offset-3 col-md-10 col-md-offset-2 main">
    		  <div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/59">Pusat Layanan PNJ</a>
		</h4>
		<p>
	Untuk mewujudkan pelayanan prima yang memberikan kepastian kepada para pemangku kepentingan, kami menggunakan sistem pelayanan terpusat yang dapat menampung permohonan layanan. Setiap permohonan layanan akan mendapatkan nomor tiket yang unik yang dapat Anda gunakan untuk melihat kemajuan permohonan layanan dan juga dapat digunakan untuk merespon secara langsung.</p>
<p>
	Sistem Pusat Layanan PNJ dapat diakses melalui halaman&nbsp;<a href="http://layanan.pnj.ac.id/" target="_blank">layanan.pnj.ac.id</a>.&nbsp;Untuk membuat permohonan layanan silahkan klik &quot;Open New Ticket&quot; atau &quot;Buka Tiket Baru&quot; kemudian pilih topik yang tersedia selanjutnya isi data yang dibutuhkan. Untuk melihat kemajuan permohonan layanan silahkan klik &quot;Check Ticket Status&quot; atau bisa melihat statusnya dari email pemohon.</p>
<p>
	Saat ini kami membuka kesempatan kepada semua Bagian / Unit / Pusat PNJ untuk dapat menggunakan aplikasi ini agar kinerja Anda dapat terekam di dalam sistem ini. Untuk informasi lebih lanjut dapat menghubungi PUSDATIN PNJ pada email pusdatin [a.t.] pnj ac id</p>
<p>
	Silahkan mencoba !</p>		</div>
</div>
<br>
<div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/58">Ucapan Belasungkawa</a>
		</h4>
		<div>
	<u><strong>Inna Lillahi wa inna ilaihi raji&#39;un</strong></u></div>
<div>
	&nbsp;</div>
<div>
	Segenap Keluarga Besar Politeknik Negeri Jakarta mengucapkan belasungkawa yang mendalam atas berpulangnya ke Rahmatullah<strong> Putra Pertama </strong>dari <strong>Bapak Andikanoza Pradiptiya, S.T., M.Eng</strong>. staf pengajar Jurusan Teknik Sipil, pada hari<strong> Selasa, 6 September 2016</strong>.</div>
<div>
	&nbsp;</div>
<div>
	Semoga Allah SWT menerima semua amal ibadahnya, dan menempatkannya di tempat yang terbaik di sisi-Nya, serta keluarga yang ditinggalkan diberikan keikhlasan, ketabahan dan kesabaran. &nbsp;Aamiin.</div>		</div>
</div>
<br>
<div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/48">Jaringan Local Area Network GIGABIT PNJ</a>
		</h4>
		<p>
	Saat ini PUSDATIN sedang melaksanakan program upgrade jaringan LAN (Local Area Network) dalam rangka meningkatkan kecepatan LAN dan internet. Mohon share hasil&nbsp;<a href="http://www.speedtest.net/" target="_blank">speedtest</a>&nbsp;anda dengan cara mention&nbsp;<a href="https://twitter.com/PusdatinPNJ" target="_blank">twitter PUSDATIN</a>&nbsp;@PusdatinPNJ atau melalui email pusdatin@pnj.ac.id sebagai bahan evaluasi kami. Berikut ini adalah titik-titik / gedung yang sudah terpasang switch GIGABIT (per 18 April 2016):</p>
<ol>
	<li>
		Teknik Informatika</li>
	<li>
		Akuntansi</li>
	<li>
		Gedung Serba Guna</li>
	<li>
		Perpustakaan</li>
	<li>
		Gedung Direktorat Lantai 2</li>
	<li>
		Teknik Mesin</li>
	<li>
		Gedung Direktorat Lantai 1</li>
	<li>
		Administrasi Bisnis</li>
	<li>
		Gedung Kearsipan</li>
	<li>
		Teknik Grafika dan Penerbitan</li>
	<li>
		Gedung D Teknik Elektro</li>
</ol>
<p>
	Untuk penggunaan wifi yang relatif stabil, dapat menggunakan wifi dengan SSID &quot;PNJ_Hotspot&quot; dengan password 0217270036 yang saat ini sudah mengcover kurang lebih 50% dari area PNJ.</p>		</div>
</div>
<br>
<div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/41">Penggunaan Bandwidth Internet PNJ</a>
		</h4>
		<p>
	PUSDATIN beberapa hari ini mencoba tidak membatasi penggunaan bandwidth, akibatnya beberapa hari ini sering terjadi akses yang melambat karena terjadi ketidak adilan penggunaan bandwidth antara satu user dengan user lainnya. Oleh karena itu PUSDATIN mengembalikan kembali ke kondisi normal (menggunakan proxy).&nbsp;Oleh karena itu mohon kepada seluruh civitas akademik PNJ agar menggunakan internet dengan bijak untuk kepentingan pendidikan bersama.</p>
<p>
	Berikut ini beberapa screenshoot penggunaan bandwidth PNJ dalam beberapa hari ini (tanpa proxy):</p>
<p>
	<img alt="" src="/upload/artikel/images/Penggunaan20151207.png" style="width: 604px; height: 245px;" /></p>
<p>
	<img alt="" src="/upload/artikel/images/Penggunaan20151210.png" style="width: 599px; height: 256px;" /></p>
<p>
	<img alt="" src="/upload/artikel/images/Penggunaan20151211.png" style="width: 605px; height: 265px;" /></p>		</div>
</div>
<br>
<div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/34">Pendaftaran Internet Mahasiswa Dibuka Kembali</a>
		</h4>
		<p>
	Renovasi ruang pusdatin telah selesai, pendaftaran internet mahasiswa sudah bisa dilakukan di loket GSG. Pendaftaran internet dibuka hari senin-jumat pukul 9:00-16:00. Istirahat pukul 12:00-13:00.</p>
<p>
	Terimakasih atas perhatiannya.</p>		</div>
</div>
<br>
<div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/4">Frequently Asked Questions (F.A.Q)</a>
		</h4>
		<p>
	<strong>Kenapa harus login sebelum mengakses internet?</strong></p>
<p>
	Untuk mempermudah manajemen pengguna internet di PNJ agar alokasi bandwidth sesuai dengan sasaran yaitu untuk civitas akademika Politeknik Negeri Jakarta.</p>
<p>
	<strong>Kenapa internet disconnect dalam waktu 5 menit?</strong></p>
<p>
	Karena halaman/tab user ditutup (sesuai pengumuman).</p>
<p>
	<strong>Kenapa internet disconnect&nbsp;</strong><strong>dalam waktu 5 menit&nbsp;</strong><strong>jika halaman/tab User ditutup?</strong></p>
<p>
	Alasan keamanan, untuk mencegah dan meminimalisir spam atau virus menggunakan koneksi internet jika user tidak menggunakan internet (atau lupa logout).</p>

			<p><a href="http://152.118.191.12/index.php/user/berita/4"><b><big>Selengkapnya >></big></b></a></p>		</div>
</div>
<br>
<div class="media">
	<div class="media-body">
		<h4 class="media-heading">
			<a href="http://152.118.191.12/index.php/user/berita/3">Tata Tertib Layanan Internet PNJ</a>
		</h4>
		<p>
	Fasilitas Layanan Internet yang terdapat di Politeknik Negeri Jakarta dimaksudkan sebagai sarana kerja, pendidikan, maupun pengabdian pada masyarakat yang dilakukan oleh pemakai yang telah terdaftar di Politeknik Negeri Jakarta. Para pemakai diharapkan pengertian dan kesadarannya untuk menjaga keutuhan dan keamanan peralatan yang ada. Kesadaran tersebut hendaknya diterapkan terhadap semua peralatan yang ada di setiap Jurusan, Unit, UPT, serta semua sistem komputasi lainnya yang dapat diakses melalui jaringan komunikasi yang tersedia. Pengelola Infrastruktur Jaringan PNJ dikelola oleh PUSDATIN yang terletak di : PUSDATIN PNJ Gd. E (GSG) Depok, dan diketuai oleh Nur Cholikul Anwar.</p>
<p>
	Pemakai yang berhak untuk menggunakan layanan internet di PNJ adalah staf akademik, staf administrasi dan mahasiswa Politeknik Negeri Jakarta. Keanggotaan Setiap pengguna layanan akses internet di PNJ wajib memiliki user account dengan mengisi form registrasi yang terdapat pada halaman login.</p>
<p>
	<strong>Periode Waktu</strong></p>
<p>
	Masa Account Layanan Internet di PNJ akan berakhir Pada :</p>
<ul>
	<li>
		Mahasiswa : akhir semester / tidak lagi kuliah di PNJ</li>
	<li>
		Staf : Jika sudah tidak lagi bekerja di PNJ</li>
</ul>

			<p><a href="http://152.118.191.12/index.php/user/berita/3"><b><big>Selengkapnya >></big></b></a></p>		</div>
</div>
<br>
    		<br>
    <footer class="footer">
	<div class="container-fluid">
		<ul class="list-inline">
			<li><a href="http://152.118.191.12/index.php/daftar/tentang_kami"
				onclick="return GB_myShow('Tentang PUSDATIN', this.href, 300,500, true)"
				title="Tentang PUSDATIN">Tentang Kami</a></li>
			<li><a href="http://152.118.191.12/index.php/user/send_message?receiver=1"
				target="_new">Kontak Kami</a></li>
			<li><small>(Anda akan terlogout secara otomatis jika menutup halaman
					ini)</small></li>
		</ul>
	</div>
</footer>			</div>
		</div>
	</div>

	<a href="javascript:void(0)" onclick="javascript:chatWith('9007')">.</a>
	<a href="javascript:void(0)" onclick="javascript:chatWith('64035')">.</a>
	<a href="javascript:void(0)" onclick="javascript:chatWith('8888')">.</a>
	<div id="main_container"></div>
	<script type="text/javascript"
		src="http://152.118.191.12/chat/js/jquery.js"></script>
	<script type="text/javascript"
		src="http://152.118.191.12/chat/js/chat.js"></script>
	<audio id="audiotag1" preload="auto"> <source
		src="http://152.118.191.12/public/sound/flute_c_long_01.wav"
		type="audio/wav"></audio>
	<a href="javascript:play_single_sound();">.</a>
</body>
</html>
