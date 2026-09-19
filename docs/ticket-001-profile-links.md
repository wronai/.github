# Ticket 001: recover profile links and cache exclusions

GitHub issue: https://github.com/wronai/.github/issues/1

Recover the two source changes from local e355a009c94b8d06af60c26c2b927f6e0f1dae19 on current main. Project names link to the GitHub repository; distinct homepages get a separate www link. Toolkit copying excludes Python bytecode and cache directories.

Keep the newer generated profile README; the next normal sync renders it with the updated generator. Preserve the original local checkout and its bytecode changes. This delivery does not run organization sync or deploy_to_orgs.sh against real repositories. Existing tracked bytecode is outside this source recovery.

Validation: offline generator scenarios (explicit homepage, inferred Pages homepage, repository URL without duplicate www link, .github filtering), bash syntax, and a disposable rsync fixture for bytecode exclusions. One isolated writer, no repository lease controller adopted; host layout record is not a fencing lease.
