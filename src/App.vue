<template>
    <div class="geral">
        <div class="header">
            <img class="img1" src="./assets/page-banner-default.png" alt="">
        </div>
        <div class="main">
            <div class="itens">
                <p>hospedagens</p>
                <p>item2</p>
                <p>item3</p>
            </div>
                <p class="title">Meus sites</p>
                <p class="txt">Aqui você encontra a lista dos seus sites existentes no plano de Hospedagem e/ou Servidores Gerenciados</p>       
            <div class="menu">
                <p>hospedagens</p>
                <p>dominios</p>
                <p>banco de dados</p>
                <p>arquivos ftp</p>
                <p>aplicativos</p>
                <p>ferramentas</p>
                <p>gerenciamento</p>
            </div>
            <div class="painel">
                <img class="img2" src="./assets/Icon.png" alt="icone ">
                <p class="txt2">Esse é o nosso novo painel de Hospedagem. Fizemos várias melhorias para aperfeiçoar sua experiência com nosso produto. Aproveite!</p>
                <img class="img2" src="./assets/seta.png" alt="seta ">
                <img class="img2" src="./assets/x.png" alt="icone de fechar">
            </div>
            <div class="filtro">
                 <input type="text" placeholder="procure seu site aqui" class="input" >
                 <button>Filtrar</button>
            </div>
            <div class="sites">
                <div class="ajuste">
                    <img class="img2" src="./assets/Draw.png" alt="seta ">
                    <img class="img2" src="./assets/windows.png" alt="seta ">
                    <div class="detalhes">
                        <p class="exemplo">siteexemplo.com.br</p>
                        <p>site ativo Usuário FTP: exemplo1</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');
.geral{display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    width: 100%;
}
.main{width: 1440px;}
.img1{width: 100%;}
.itens{
margin-top: 30px;
display: flex;
justify-content: space-between;
width: 200px;
height: 18px;
font-family: 'Ubuntu', sans-serif; 
font-style: normal;
font-weight: 400;
font-size: 15px;
line-height: 150%
}
.title{
margin-top: 30px;
font-family: 'Ubuntu';
font-style: normal;
font-weight: 500;
font-size: 34px;
line-height: 150%;
color: #424242;
 }
 .txt{
font-family: 'Ubuntu';
font-style: normal;
font-weight: 400;
font-size: 20px;
line-height: 150%;
color: #636466;
}
.menu{
margin-top: 40px;
display: flex;
justify-content: space-between;
align-items: center;
padding: 0px 180px;
 height: 53px;
width: 1440px;
background: #FFFFFF;
border: 1px solid #EEEEEE;
font-family: 'Ubuntu';
font-style: normal;
font-weight: 400;
font-size: 17px;
line-height: 150%
}
.painel{
box-sizing: border-box;
display: flex;
 align-items: flex-start;
padding: 16px;
gap: 16px;
position: absolute;
width: 1080px;
height: 80px;
margin-top: 30px;
background: #FFFFFF;
border-left: 4px solid #43A047;
box-shadow: 0px 2px 2px rgba(33, 33, 33, 0.25);
border-radius: 4px;
font-family: 'Ubuntu', sans-serif; 
font-style: normal;
font-weight: 500;
font-size: 20px;
line-height: 150%;
display: flex;
align-items: center;
color: #424242;
}
.filtro{
    display: flex;
    justify-content: space-between;
    width: 444px;
    margin-top: 160px;
}
.input{
Width:320px;
height: 77px;
border-color: #424242;
}
button{width: 120px;
height: 60px;
color: white;
background: red;
}
.sites{height: 81px;
width: 1080px;
left: 180px;
top: 433px;
border-radius: 8px;
padding: 16px;
background: #FFFFFF;
border: 1px solid #EEEEEE;
/* shadows/box-shadow-raised */

box-shadow: 0px 2px 2px rgba(33, 33, 33, 0.25);
border-radius: 8px;
}
.ajuste{     display: flex;
    justify-content: space-between;
    width: 454px;
}

.exemplo{
  font-size: 30px;
  }
 </style>