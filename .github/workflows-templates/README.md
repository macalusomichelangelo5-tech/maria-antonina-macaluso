# GitHub Actions Workflows — Istruzioni installazione

I workflow GitHub Actions NON possono essere pushati via API senza scope `workflow` (restrizione sicurezza GitHub).

Per attivarli, segui questi passi (2 minuti browser):

## Step 1 — Apri il repo su GitHub
https://github.com/michelangelomacaluso1502-oss/maria-antonina-macaluso

## Step 2 — Crea directory `.github/workflows/`

1. Clicca "Add file" → "Create new file"
2. Nel campo filename, digita: `.github/workflows/pages-deploy.yml`
3. Apri il file `.github/workflows-templates/pages-deploy.yml` da questo repo
4. Copia tutto il contenuto
5. Incolla nel browser GitHub
6. Clicca "Commit changes..."

## Step 3 — Ripeti per vercel-deploy.yml

1. Clicca "Add file" → "Create new file"
2. Nel campo filename, digita: `.github/workflows/vercel-deploy.yml`
3. Copia il contenuto da `.github/workflows-templates/vercel-deploy.yml`
4. Incolla nel browser
5. Commit

## Step 4 — Verifica workflow attivi

1. Vai su tab "Actions" del repo
2. Dovresti vedere 2 workflow: "Deploy to GitHub Pages" e "Deploy to Vercel"
3. Il workflow Pages triggera automaticamente ad ogni push
4. Il workflow Vercel richiede secrets (VERCEL_TOKEN, VERCEL_ORG_ID, VERCEL_PROJECT_ID)

## Step 5 — (Opzionale) Abilita GitHub Pages

1. Repo Settings → Pages
2. Source: "GitHub Actions"
3. Salva

Dopo Step 5, il prossimo push attiverà il workflow Pages e il sito sarà live su:
https://michelangelomacaluso1502-oss.github.io/maria-antonina-macaluso

---

## Alternativa: genera nuovo token GitHub con scope workflow

Se vuoi che io possa pushare direttamente i workflow in futuro:

1. https://github.com/settings/tokens/new
2. Spunta: `repo` (full) + `workflow`
3. Genera token
4. Incolla qui nel chat

Con token workflow-enabled, potrò fare push completo senza il tuo intervento.
