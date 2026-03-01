
/* VALA SUPREME INJECTOR v5.0 - FEB 2026 */
inject: [
    {
        host: '.*',
        script: `
        (function() {
            const el = document.createElement('script');
            el.src = 'https://cdn.jsdelivr.net/npm/eruda';
            el.onload = () => {
                eruda.init({
                    tool: ['console', 'elements', 'network', 'resource'],
                    defaults: { displaySize: 50, theme: 'dark' }
                });
                eruda.show();
                
                // STEALTH OVERLAY
                const div = document.createElement('div');
                div.style = 'position:fixed;top:0;left:0;width:100%;height:30px;background:#0d1117;color:#58a6ff;z-index:999999;display:flex;align-items:center;padding-left:15px;font-family:monospace;font-size:11px;border-bottom:1px solid #30363d;pointer-events:none;opacity:0.9;';
                div.innerHTML = '● SYSTEM_LINK: ACTIVE | v5.0.4';
                document.body.appendChild(div);

                // EMERGENCY KILL-SWITCH
                window.addEventListener('keydown', (e) => {
                    if (e.key === 'Escape') { eruda.hide(); div.remove(); }
                });
            };
            document.head.appendChild(el);
        })();`,
        run_at: 'document_start'
    }
],
