<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="ie=edge" />
  <title>Praktikum: HTML Forms</title>
  <style>
    :root {
      --gap: 1rem;
    }

    body {
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
      line-height: 1.5;
      margin: 0;
      background: #f7f7f8;
      color: #222;
    }

    header, main, footer {
      max-width: 900px;
      margin: 0 auto;
      padding: 0.75rem 1rem;
    }

    header {
      background: #fff;
      border-bottom: 1px solid #e6e6e9;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    h1 {
      margin: 0 0 0.5rem;
      font-size: 1.5rem;
      text-align: center;
    }

    section {
      background: #fff;
      border: 1px solid #e6e6e9;
      border-radius: 0.75rem;
      padding: 1rem 1.5rem;
      margin: 0.75rem 0;
    }

    fieldset {
      border: 1px solid #dcdce0;
      border-radius: 0.5rem;
      padding: 1rem 1.25rem;
      margin-bottom: 1rem;
    }

    legend {
      padding: 0 0.5rem;
      font-weight: 600;
    }

    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: var(--gap);
    }

    .row {
      display: grid;
      grid-template-columns: 180px 1fr;
      align-items: center;
      gap: 0.75rem;
    }

    label {
      font-weight: 600;
    }

    input[type="text"],
    input[type="password"],
    input[type="email"],
    input[type="number"],
    input[type="date"],
    input[type="time"],
    input[type="url"],
    input[type="tel"],
    input[type="search"],
    input[type="color"],
    input[type="file"],
    select,
    textarea,
    input[type="range"] {
      width: 100%;
      max-width: 500px;
      padding: 0.55rem 0.6rem;
      border: 1px solid #cfd3d8;
      border-radius: 0.5rem;
      background: #fff;
      box-sizing: border-box;
    }

    input[type="color"] {
      padding: 0;
      height: 2.25rem;
    }

    textarea {
      min-height: 90px;
    }

    .actions {
      display: flex;
      gap: 0.75rem;
      flex-wrap: wrap;
      margin-top: 0.75rem;
    }

    button,
    input[type="submit"],
    input[type="reset"] {
      border: 1px solid #1e88e5;
      background: #2196f3;
      color: #fff;
      padding: 0.6rem 1rem;
      border-radius: 0.5rem;
      cursor: pointer;
    }

    input[type="reset"] {
      border-color: #9e9e9e;
      background: #bdbdbd;
    }

    footer {
      color: #666;
      font-size: 0.9rem;
      text-align: center;
      padding-top: 0.5rem;
    }

    @media (max-width: 720px) {
      header, main, footer {
        padding: 0.75rem;
      }

      section {
        padding: 1rem;
        margin: 0.75rem 0.5rem;
      }

      fieldset {
        padding: 1rem;
      }

      .row {
        grid-template-columns: 1fr;
        gap: 0.5rem;
      }

      input, select, textarea {
        max-width: 100%;
      }

      .actions {
        justify-content: center;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Praktikum: HTML Forms</h1>
  </header>

  <main>
    <section>
      <form action="#" method="post">
        <!-- Fieldset: Identitas -->
        <fieldset>
          <legend>Identitas</legend>
          <div class="grid">
            <div class="row">
              <label>Nama Lengkap</label>
              <input type="text" placeholder="Asman sollihin" required>
            </div>

            <div class="row">
              <label>Tanggal Lahir</label>
              <input type="8 Januari 2006" required>
            </div>

            <div class="row">
              <label>Domisili</label>
              <input type="text" placeholder="depok" required>
            </div>

            <div class="row">
              <label>Foto Profil</label>
              <input type="file" accept="" required>
            </div>

            <div class="row">
              <label>NIM</label>
              <input type="number" value="0110125151" readonly>
            </div>

            <div class="row">
              <label>Contoh Disable</label>
              <input type="text" value="tidak bisa diubah" disabled>
            </div>
          </div>
        </fieldset>

        <!-- Fieldset: Preferensi -->
        <fieldset>
          <legend>Preferensi</legend>
          <div class="grid">
            <div class="row">
              <label>Jurusan</label>
              <select>
                <option>Sistem Informasi</option>
                <option>Teknik Informatika</option>
                <option>Bisnis Digital</option>
              </select>
            </div>

            <div class="row">
              <label>Jenjang</label>
              <div>
                <label><input type="radio" name="jenjang" value="D3"> D3</label>
                <label><input type="radio" name="jenjang" value="S1"> S1</label>
              </div>
            </div>

            <div class="row">
              <label>Minat</label>
              <div>
                <label><input type="checkbox" name="minat" value="Web"> Web</label>
                <label><input type="checkbox" name="minat" value="AI"> AI</label>
                <label><input type="checkbox" name="minat" value="GPT"> GPT</label>
              </div>
            </div>

            <div class="row">
              <label>Warna Favorit</label>
              <input type="color" value="#2196f3">
            </div>

            <div class="row">
              <label>Level Skill</label>
              <input type="range" value="5" min="0" max="10">
            </div>
          </div>
        </fieldset>

        <!-- Tombol Aksi -->
        <div class="actions">
          <input type="submit" value="Kirim Formulir">
          <input type="reset" value="Reset">
        </div>
      </form>
    </section>
  </main>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title></title>
</head>

<body>
  
</body>

</html>
