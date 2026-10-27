# agentic-coder

Danışarak kodlama skill'i / plugin'i.

Aktifken Claude yalnızca açıkça yönlendirilen işi yapar: iş kuralı, mimari karar
veya belirsiz teknik konularda varsaymak yerine kullanıcıdan onay ister.

## Kurulum

### Claude Code

```bash
git clone git@github.com:lKhanl/agentic-coder.git ~/.claude/skills/agentic-coder
```

Sonraki Claude Code oturumunda otomatik yüklenir (`agentic-coder@skills-dir`).

### Codex

`~/.codex/plugins/` altına klonla (Codex'in plugin dizinini kullanıyorsan) veya
`.codex-plugin/plugin.json` manifestini referans alarak kendi kurulum yönteminle ekle.

### OpenCode

`opencode.json` dosyana ekle:

```json
{
  "plugin": ["agentic-coder@git+https://github.com/lKhanl/agentic-coder.git"]
}
```

Detaylar için [.opencode/INSTALL.md](.opencode/INSTALL.md).

### Antigravity (AGY)

**Skills CLI ile (Önerilen):**
```bash
npx skills add lKhanl/agentic-coder -g -y
```

**Git Clone ile:**
```bash
git clone https://github.com/lKhanl/agentic-coder.git ~/.agents/skills/agentic-coder
```

## Yapı

```
.claude-plugin/plugin.json   ← Claude Code manifest
.codex-plugin/plugin.json    ← Codex manifest
.opencode/                   ← OpenCode plugin + kurulum talimatı
skills/agentic-coder/SKILL.md ← kural içeriği (tüm araçların ortak kaynağı)
```
