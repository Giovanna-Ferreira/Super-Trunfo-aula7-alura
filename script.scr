var champ1 = {
    nome: "Akali",
    atributos: {
     ataque: 65,
     defesa: 7,
     magia: 9
   }
  };
  
  var champ2 = {
    nome: "Sett",
    atributos: {
     ataque: 80,
     defesa: 32,
     magia: 9
   }
  };
  
  var champ3 = {
    nome: "Lillia",
    atributos: {
     ataque: 18,
     defesa: 10,
     magia: 56
   }
  };
  
  var champ4 = {
    nome: "Ezreal",
    atributos: {
     ataque: 35,
     defesa: 27,
     magia: 38
   }
  };
  
  var champ5 = {
    nome: "Rammus",
    atributos: {
     ataque: 62,
     defesa: 85,
     magia: 30
   }
  };
  var champ6 = {
    nome: "Yummi",
    atributos: {
     ataque: 32,
     defesa: 27,
     magia: 74
   }
  };
  
  var atributos = [champ1, champ2, champ3, champ4, champ5, champ6];
  var campeaoMaquina;
  var campeaoJogador;
  
  function sortearCarta() {
    var numeroCampeaoMaquina = parseInt(Math.random() * 6);
    campeaoMaquina = atributos[numeroCampeaoMaquina];
    
    var numeroCampeaoJogador = parseInt(Math.random() * 6);
    while (numeroCampeaoMaquina == numeroCampeaoJogador) {
    numeroCampeaoJogador = parseInt(Math.random() * 6);
  }
  campeaoJogador = atributos[numeroCampeaoJogador];
  console.log(campeaoJogador);
  
  document.getElementById("btnSortear").disabled = true;
  document.getElementById("btnJogar").disabled = false;
    
  exibirOpcoes();
  }
    
  function exibirOpcoes() {
    var opcoes = document.getElementById("opcoes");
    var opcoesTexto = "";
    
    for (var campeao in campeaoJogador.atributos) {
         opcoesTexto +=
        "<input type='radio' name='campeao' value='" + campeao + "'>" + campeao;
    }
    opcoes.innerHTML = opcoesTexto;
  }
  
  function obtemCampeaoSelecionado() {
    var radioCampeoes = document.getElementsByName("campeao");
    
    for(var i = 0; i < radioCampeoes.length; i++) {
      if (radioCampeoes[i].checked == true) {
        return radioCampeoes[i].value;
      }
    }
  }
  
  function jogar() {
    var campeaoSelecionado = obtemCampeaoSelecionado();
    var elementoResultado =  document.getElementById("resultado");
    var valorCampeaoJogador = campeaoJogador.atributos[campeaoSelecionado];
    var valorCampeaoMaquina = campeaoMaquina.atributos[campeaoSelecionado];
    
    if (valorCampeaoJogador > valorCampeaoMaquina) {
      elementoResultado.innerHTML = "Você é mais forte nessa categoria que esse campeão, parabêns invocador";
    } else if (valorCampeaoMaquina > valorCampeaoJogador) {
      elementoResultado.innerHTML = "Ihh... Foi de base!, o bot era mais forte que você";
    } else {
      elementoResultado.innerHTML = "a quantidade do poder são idêndicos! Temos um empate!";
     console.log(campeaoMaquina);
    }
  }
