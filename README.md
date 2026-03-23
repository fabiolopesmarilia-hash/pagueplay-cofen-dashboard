# pagueplay-cofen-dashboard
Dashboard de Cobrança COFEN/PaguePlay
// ── RESTORE import badges on load ──
function restoreImportBadges(){
  if(localStorage.getItem('cofen_import_rec_done')){ const b=document.getElementById('imp-rec-badge'); if(b) b.style.display='block'; }
  if(localStorage.getItem('cofen_import_ac_done')){ const b=document.getElementById('imp-ac-badge'); if(b) b.style.display='block'; }
}

// ── INIT ──
loadSavedOverrides();
loadGestaoOverrides();
loadSharedPhotos();
restoreImpor  // <-- INCOMPLETE!
// ── COMPLETE INITIALIZATION ──
function initialize() {
  loadSavedOverrides();
  loadGestaoOverrides();
  loadSharedPhotos();
  restoreImportBadges();
  initHero();
  buildCal('cal-grid');
  buildCal('cal-grid2');
  mkGD();
  mkDist();
  mkTop5();
  mkEq();
  buildOpEditor();
  tick();
  setInterval(tick, 1000);
  fbAutoConnect();
  impTab('rec');
  toast('✅ Dashboard carregado!');
}

// Run on DOM ready
document.addEventListener('DOMContentLoaded', initialize);
    </script>
  </body>
</html>
