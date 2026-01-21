# dokploy-templates-ia

Collection de blueprints Dokploy pour une stack IA modulaire.

Structure:
- blueprints/base-stack/: socle mutualisé (Supabase, Redis, MinIO/S3-compatible)\n- blueprints/ia-stack/: blueprint monolithique contenant tous les services (décomposable en blueprints par service)\n- blueprints/<service>/: dossiers placeholder par service (contiennent template.toml indiquant comment utiliser le service via base-stack ou ia-stack)

Usage rapide:
1. Déployer d'abord le blueprint `base-stack` dans Dokploy pour créer Supabase, Redis et le stockage S3 (Infomaniak).\n2. Déployer ensuite `ia-stack` ou les blueprints de services individuels.\n
Licence: MIT (identique à Dokploy/templates)