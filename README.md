<!-- Dentro do <div class="carrinho">, logo após o select de pagamento -->
<div id="pix-info" style="display:none; margin-bottom: 15px; padding: 10px; background:#e0f7fa; border-radius:8px;">
    <p><strong>Pagamento via Pix</strong></p>
    <p>Chave Pix: <code>5548999541113</code></p>
    <p>Clique no botão para copiar a chave Pix:</p>
    <button onclick="copiarPix()">Copiar Chave Pix</button>
    <div style="margin-top:10px;">
      <img id="pix-qr" src="https://chart.googleapis.com/chart?cht=qr&chs=180x180&chl=00020126360014BR.GOV.BCB.PIX01135548999541113025802BR5913Cantina Tezzari6009Sao Paulo62100508Pagamento520400005303986540440005802BR5925Cantina Tezzari - Delivery6009Sao Paulo62070503***6304B4F5" alt="QR Code Pix">
    </div>
</div>

<script>
    // Função para mostrar/ocultar Pix dependendo da forma de pagamento
    const pagamentoSelect = document.getElementById('pagamento');
    const pixInfo = document.getElementById('pix-info');

    pagamentoSelect.addEventListener('change', () => {
        if(pagamentoSelect.value === 'Pix'){
            pixInfo.style.display = 'block';
        } else {
            pixInfo.style.display = 'none';
        }
    });

    // Função para copiar a chave Pix
    function copiarPix() {
        const chavePix = '5548999541113';
        navigator.clipboard.writeText(chavePix).then(() => {
            alert('Chave Pix copiada para a área de transferência!');
        }, () => {
            alert('Falha ao copiar a chave Pix.');
        });
    }
</script>
