# Rust template

Lekki szablon projektu w Rust, który działa „out of the box” i wymusza podstawowe nawyki: formatowanie, linty i testy.

## Jak zacząć
1. Użyj przycisku **Use this template** na GitHubie **lub**:
   ```bash
   cargo generate --git https://github.com/Rust-Lab-PJATK/rust-template --name my-app
   ```
2. Zainstaluj toolchain Rust (stable) i `cargo`.
3. Lokalnie przed commitem uruchom:
   ```bash
   cargo fmt
   cargo clippy -- -D warnings
   cargo test
   ```

## Zawartość
- `src/main.rs` – przykładowa aplikacja binarna.
- `tests/basic.rs` – przykładowy test pokazujący strukturę `tests/`.
- `rustfmt.toml` – wspólne ustawienia formatowania (szerokość 100, edition 2024).
- `.github/workflows/ci.yml` – CI z fmt, clippy, testami.
- `.pre-commit-config.yaml` – lokalny git hook (fmt, clippy, test na push).
- `.gitignore` – ignoruje `target/`, IDE itp.

## Konwencje
- Kod przechodzi `cargo fmt` i `cargo clippy -- -D warnings` zanim trafi do PR.
- CI musi być zielone.
- Brak zbędnych zależności w `Cargo.toml` – to ma być czysty start.

## Opcjonalnie
- Pre-commit: zainstaluj `pre-commit` i uruchom `pre-commit install`; na `pre-commit run --all-files` odpala fmt + clippy, a testy na hooku `pre-push`.
- Dodaj `just` / `make`, jeśli wolisz skróty do poleceń.

## Struktura katalogów
```
.
├─ .github/workflows/ci.yml
├─ src/main.rs
├─ tests/basic.rs
├─ Cargo.toml
├─ Cargo.lock
├─ rustfmt.toml
└─ .gitignore
```
