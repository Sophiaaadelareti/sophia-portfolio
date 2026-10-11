document.addEventListener('DOMContentLoaded', () => {
    const menuBtn = document.getElementById('menu');
    const configBtn = document.getElementById('config');
    const modalMenu = document.getElementById('modalPáginas');
    const modalConfig = document.getElementById('modalEscuro');
    const btnEscuro = document.getElementById('BotaoEscuro');

    menuBtn?.addEventListener('click', (e) => {
        e.stopPropagation(); // Evita que o clique feche imediatamente
        modalMenu.classList.toggle('Ativo');
        modalConfig.classList.remove('Ativo');
    });

    configBtn?.addEventListener('click', (e) => {
        e.stopPropagation();
        modalConfig.classList.toggle('Ativo');
        modalMenu.classList.remove('Ativo');
    });

    document.addEventListener('click', (e) => {
        if (modalMenu && !modalMenu.contains(e.target) && !menuBtn.contains(e.target)) {
            modalMenu.classList.remove('Ativo');
        }
        if (modalConfig && !modalConfig.contains(e.target) && !configBtn.contains(e.target)) {
            modalConfig.classList.remove('Ativo');
        }
    });

    if (localStorage.getItem('darkMode') === 'true') {
        document.body.classList.add('Escuro');
        btnEscuro?.classList.add('Ativo');
    }

    btnEscuro?.addEventListener('click', () => {
        document.body.classList.toggle('Escuro');
        btnEscuro.classList.toggle('Ativo');

        const isDark = document.body.classList.contains('Escuro');
        localStorage.setItem('darkMode', isDark);
    });
});