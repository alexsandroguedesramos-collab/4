<!-- index.html -->
<button class="btn-tema-escuro">🌙</button>
<button class="btn-voltar-topo">⬆️</button>

<!-- style.css -->
<style>
.btn-voltar-topo {
    position: fixed;
    bottom: 80px;
    right: 16px;
    font-size: 24px;
    padding: 12px;
    background-color: var(--cor-secundaria);
    border: none;
    border-radius: 50%;
    cursor: pointer;
}
</style>

<!-- script.js -->
<script>
const btnVoltarTopo = document.querySelector(".btn-voltar-topo");

btnVoltarTopo.addEventListener("click", function () {
    window.scrollTo(0, 0);
});
</script>
