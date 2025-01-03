<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Metode SAW</title>
    <link rel="stylesheet" href="./bootstrap.min.css">
    <script src="./jquery.js"></script>
  </head>
  <body class="container mt-4">
    <div class="card mb-3">
        <div class="card-header">
            <h3>Form kolom untuk kategori</h3>
        </div> 
        <div class="card-body">
          <div class="row mb-3">
              <div class="col">
                  <input type="text" id="namaKolom" class="form-control" placeholder="Nama Kriteria">
              </div>
              <div class="col">
                  <input type="number" id="bobotKolom" class="form-control" placeholder="Bobot (0-1)" step="0.1" min="0" max="1">
              </div>
              <div class="col">
                  <select id="tipeKolom" class="form-control">
                      <option value="benefit">Benefit</option>
                      <option value="cost">Cost</option>
                  </select>
              </div>
              <div class="col">
                  <button onclick="tambahKolomKeDaftar()" class="btn btn-primary">Tambah Kriteria</button>
              </div>
          </div>
          <div class="row mb-3">
              <div class="col">
                  <h5>Daftar Kriteria:</h5>
                  <ul id="daftarKolom" class="list-group"></ul>
              </div>
          </div>
        </div>

    </div>

    <div class="card mb-3">
      <div class="card-header">
        <h3>Form baris untuk data</h3>
      </div>

      <div class="card-body">
        <div id="formInputBaris" class="row mb-3 d-none">
            <div class="col">
                <h5>Input:</h5>
                <div id="fieldInputBaris"></div>
                <button onclick="simpanDataBaris()" class="btn btn-success mt-2">Simpan</button>
            </div>
        </div>
    
        <div class="row mb-3">
            <div class="col">
                <button onclick="tampilkanFormInputBaris()" class="btn btn-success">Tambah</button>
                <button onclick="hitungSAW()" class="btn btn-warning">Hitung SAW</button>
            </div>
        </div>
        <div class="row mb-3">
            <div class="col">
                <h5>Data:</h5>
                <ul id="daftarBaris" class="list-group"></ul>
            </div>
        </div>
      </div>
    </div>

    <div id="hasilContainer"></div>

    <script>
        let kolom = ['No', 'Nama'];
        let bobot = [0, 0];
        let tipe = ['none', 'none'];
        let baris = [];
        let jumlahBaris = 0;

        function tambahKolomKeDaftar() {
            const namaKolom = $('#namaKolom').val();
            const bobotKolom = parseFloat($('#bobotKolom').val());
            const tipeKolom = $('#tipeKolom').val();
            
            if (namaKolom && !isNaN(bobotKolom)) {
                kolom.push(namaKolom);
                bobot.push(bobotKolom);
                tipe.push(tipeKolom);
                
                $('#daftarKolom').append(`
                    <li class="list-group-item">
                        ${namaKolom} (Bobot: ${bobotKolom}, Tipe: ${tipeKolom})
                    </li>
                `);
                
                $('#namaKolom').val('');
                $('#bobotKolom').val('');
            }
        }

        function tampilkanFormInputBaris() {
            let fieldInput = '';
            kolom.forEach((kol, index) => {
                if (kol === 'No') {
                    fieldInput += `
                        <div class="mb-2">
                            <label>${kol}</label>
                            <input type="text" class="form-control" id="baris_${index}" value="${jumlahBaris + 1}" readonly>
                        </div>`;
                } else {
                    fieldInput += `
                        <div class="mb-2">
                            <label>${kol}</label>
                            <input class="form-control" id="baris_${index}" ${index > 1 ? 'type="number"' : 'type="text"'}>
                        </div>`;
                }
            });
            $('#fieldInputBaris').html(fieldInput);
            $('#formInputBaris').removeClass('d-none');
        }

        function simpanDataBaris() {
            jumlahBaris++;
            let dataBaris = [];
            kolom.forEach((kol, index) => {
                dataBaris.push($(`#baris_${index}`).val() || '');
            });
            baris.push(dataBaris);
            
            $('#daftarBaris').append(`
                <li class="list-group-item"> ${jumlahBaris}: ${dataBaris.join(', ')}</li>
            `);
            $('#formInputBaris').addClass('d-none');
        }

        function hitungSAW() {
            let matriksKeputusan = `
                <h4>1. Matriks Keputusan</h4>
                <table class="table table-bordered mb-4">
                    <thead>
                        <tr>
                            ${kolom.map(kol => `<th>${kol}</th>`).join('')}
                        </tr>
                        <tr>
                            <th colspan="2">Bobot</th>
                            ${bobot.slice(2).map(b => `<th>${b}</th>`).join('')}
                        </tr>
                        <tr>
                            <th colspan="2">Tipe</th>
                            ${tipe.slice(2).map(t => `<th>${t}</th>`).join('')}
                        </tr>
                    </thead>
                    <tbody>
                        ${baris.map(baris => `
                            <tr>
                                ${baris.map(sel => `<td>${sel}</td>`).join('')}
                            </tr>
                        `).join('')}
                    </tbody>
                </table>
            `;

            
            let normalisasi = [];
            let tabelNormalisasi = `
                <h4>2. Matriks Normalisasi</h4>
                <table class="table table-bordered mb-4">
                    <thead>
                        <tr>${kolom.map(kol => `<th>${kol}</th>`).join('')}</tr>
                    </thead>
                    <tbody>
            `;

            for(let i = 0; i < baris.length; i++) {
                let barisNormalisasi = [];
                tabelNormalisasi += '<tr>';
                
                for(let j = 0; j < kolom.length; j++) {
                    if(j <= 1) {
                        barisNormalisasi.push(baris[i][j]);
                        tabelNormalisasi += `<td>${baris[i][j]}</td>`;
                        continue;
                    }
                    
                    let nilaiKolom = baris.map(b => parseFloat(b[j]));
                    let nilai = parseFloat(baris[i][j]);
                    let nilaiNormalisasi;
                    let rumusSementara;
                    
                    if(tipe[j] === 'benefit') {
                        let max = Math.max(...nilaiKolom);
                        nilaiNormalisasi = nilai/max;
                        rumusSementara = '(' + nilai + ' / ' + max + ')';
                    } else if(tipe[j] === 'cost') {
                        let min = Math.min(...nilaiKolom);
                        nilaiNormalisasi = min/nilai;
                        rumusSementara = '(' + min + ' / ' + nilai + ')';
                    }
                    
                    barisNormalisasi.push(nilaiNormalisasi);
                    tabelNormalisasi += `<td> <b>${rumusSementara}</b> ${nilaiNormalisasi.toFixed(4)}</td>`;
                }
                
                normalisasi.push(barisNormalisasi);
                tabelNormalisasi += '</tr>';
            }
            tabelNormalisasi += '</tbody></table>';


            let tabelBobot = `
                <h4>3. Matriks Normalisasi Terbobot</h4>
                <table class="table table-bordered mb-4">
                    <thead>
                        <tr>${kolom.map(kol => `<th>${kol}</th>`).join('')}</tr>
                    </thead>
                    <tbody>
            `;

            let preferensi = normalisasi.map((baris, i) => {
                let skor = 0;
                tabelBobot += '<tr>';
                
                for(let j = 0; j < kolom.length; j++) {
                    if(j <= 1) {
                        tabelBobot += `<td>${baris[j]}</td>`;
                        continue;
                    }
                    let nilaiTerbobot = baris[j] * bobot[j];
                    skor += nilaiTerbobot;
                    tabelBobot += `<td> <b>(${baris[j].toFixed(4)} * ${bobot[j].toFixed(4)})</b> ${nilaiTerbobot.toFixed(4)}</td>`;
                }
                
                tabelBobot += '</tr>';
                return {
                    no: baris[0],
                    nama: baris[1],
                    skor: skor
                };
            });
            tabelBobot += '</tbody></table>';

            
            preferensi.sort((a, b) => b.skor - a.skor);
            let tabelPeringkat = `
                <h4>4. Hasil Perankingan</h4>
                <table class="table table-bordered">
                    <thead>
                        <tr>
                            <th>Ranking</th>
                            <th>No</th>
                            <th>Nama</th>
                            <th>Nilai Akhir</th>
                        </tr>
                    </thead>
                    <tbody>
                        ${preferensi.map((pref, index) => `
                            <tr>
                                <td>${index + 1}</td>
                                <td>${pref.no}</td>
                                <td>${pref.nama}</td>
                                <td>${pref.skor.toFixed(4)}</td>
                            </tr>
                        `).join('')}
                    </tbody>
                </table>
            `;

            $('#hasilContainer').html(matriksKeputusan + tabelNormalisasi + tabelBobot + tabelPeringkat);
        }
    </script>
</body>
</html>
