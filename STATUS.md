# news-image-20261117 — STATUS (18 Nov 2026, ~21:15 WIB)

Bounty: "Sum up 17 November's world news in one image", $250, 50 places paid.
Deadline: **19 Nov 2026 00:00 UTC = 19 Nov 07:00 WIB** (~9 jam lagi). 8.150 entry.
Repo (BELUM DIBUAT — harus dibuat via browser): `Rzpctr2/makefun-news-image-20261117`
(dibuat setelah competition open 17 Nov 23:43 UTC — buat sekarang memenuhi syarat).

## Yang sudah jadi
- Front page broadsheet 1024×1024 (`entry.png`, 809 KiB < 1 MiB), 16 berita
  terverifikasi dari laporan 17 Nov 2026, lead "UKRAINE HITS THE CRIMEA BRIDGE",
  peta dunia + 6 pin bernomor, hierarki keterbacaan dulu (bukan kejar 50 berita).
- Dibuat dengan kode: `generate.mjs` (Node + @resvg/resvg-js) dari `news.json`
  (SVG → PNG). `main.ts` hanya meng-copy `entry.png` → `/output/entry.png`
  (diizinkan eksplisit oleh brief). Determinisme terverifikasi: 2× run,
  sha256 sama (85ce1357…).
- Local git repo, HEAD saat ini: `5b9cf589444d5f6282f5e395d9550861a4ed3550`
  (commit awal 544e7e8b + fix LICENSE SPDX).
- Bundle v2: `~/workspace/makefun/news-image-20261117-bundle-v2.tar.gz`
  sha256 `65e9eb0d54b5d21030caa3260bee203ac97fd059ac70814ce54fc7417625d8d7`
- Check lokal: 11 pass, 5 skip, 5 submission (butuh GitHub) — **SATU fail:
  `thinking_priced`** (usage rows belum ada; lihat bawah).
  thinking_reproduces 306/311 = **98,3%**; transcripts_run_record PASS.

## SISA LANGKAH (parent — urut)
1. Buat repo GitHub via browser: `Rzpctr2/makefun-news-image-20261117`, public.
2. Push file TEKS via connector push-files (butuh approval user per call):
   main.ts, generate.mjs, news.json, entry.svg, README.md, LICENSE,
   package.json, .makefun/owner.json (+ STATUS.md ini boleh ikut).
3. Upload file BINER via browser web UI (connector menolak biner):
   `entry.png` (809 KiB) ke root repo.
4. Set repo About via browser: description "A one-image summary of the
   world's news on Tuesday, 17 November 2026 — a broadsheet front page.",
   homepage `https://make.fun/bounty/news-image-20261117`,
   topics `ai-agents, bounties, games, makefun`.
5. SETELAH subagent ini selesai: query usage aggregate lalu rebuild bundle:
   - `muse.db`: SELECT ... WHERE agent_id IN ('9452b3c5-0143-4bba-bbb1-d0d097881481')
     GROUP BY agent_id (sum tokens, max message_id/created_at, model) →
     tulis 1 baris JSONL ke `~/workspace/makefun/muse-usage-news-image.jsonl`
   - Rebuild bundle v3 = perintah bundle v2 + `--muse-usage ~/workspace/makefun/muse-usage-news-image.jsonl`
   - Re-run check (harus hijau penuh, ok:true).
6. Submit (kit news-image-20261117):
   `node ~/workspace/makefun/kit-news-image-20261117/news-image-20261117-kit/cli/makefun.mjs submit --competition news-image-20261117 --repo-url https://github.com/Rzpctr2/makefun-news-image-20261117 --commit <HEAD> --bundle ~/workspace/makefun/news-image-20261117-bundle-v3.tar.gz --keypair ~/workspace/makefun/makefun-keypair.json --title "The World in One Day — 17 November 2026" --json`
   Lalu cek `status --submission <id> --json` setelah ~25 dtk.
   Simpan submission ID + claim code di sini + laporkan ke user satu baris.
