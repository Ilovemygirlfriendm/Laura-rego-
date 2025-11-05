🔍Script bookmarklet

* **Com esse script você consegue ativar o copiar e colar de áreas de texto que não tem como fazer isso. Exemplo:
Sala do futuro redação.**

javascript:(function(){function pasteHandler(e){var text='';if(e.clipboardData) text=e.clipboardData.getData('text/plain');else if(window.clipboardData) text=window.clipboardData.getData('Text');var target=document.activeElement;try{if(target&&(target.tagName==='INPUT'||target.tagName==='TEXTAREA'||target.isContentEditable)){if(typeof target.selectionStart==='number'){var start=target.selectionStart,end=target.selectionEnd,val=target.value;target.value=val.slice(0,start)+text+val.slice(end);var pos=start+text.length;target.selectionStart=target.selectionEnd=pos;}else{var sel=window.getSelection();if(sel.rangeCount){sel.deleteFromDocument();sel.getRangeAt(0).insertNode(document.createTextNode(text));}}} }catch(err){}e.stopImmediatePropagation();e.preventDefault();}document.addEventListener('paste',pasteHandler,true);document.querySelectorAll('[onpaste]').forEach(function(el){el.removeAttribute('onpaste');});alert('Colar reabilitado nesta p%C3%A1gina. Tente Ctrl+V (ou Cmd+V).');})();

* **Edita automaticamente a foto e o nome do site aberto para "Sala do futuro".**.

javascript:(function() { var l = document.querySelector("link[rel*='icon']") || document.createElement('link'); l.type = 'image/x-icon'; l.rel = 'shortcut icon'; l.href = 'https://edusp-static.ip.tv/sala-do-futuro/conteudo_logo.png'; document.getElementsByTagName('head')[0].appendChild(l); document.title = 'Sala do Futuro Aluno'; })();

Vou testar se esse email corporativo da pra logar no chromebook depois de formatar

https://emailestudante.com.br/
