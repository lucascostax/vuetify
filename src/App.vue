<template>
  <div class="geral">
    <div class="header">
      <img class="img1" src="./assets/page-banner-default.png" alt="" />
    </div>
    <div class="main">
      <div class="itens">
        <p>hospedagens</p>
        <p>item2</p>
        <p>item3</p>
      </div>
      <p class="title">Meus sites</p>
      <p class="txt">
        Aqui você encontra a lista dos seus sites existentes no plano de
        Hospedagem e/ou Servidores Gerenciados
      </p>
      <div class="text-center">
        <v-tabs fixed-tabs bg-color="indigo-darken-2">
          <v-tab> Hospedagens </v-tab>
          <v-tab> Domínios </v-tab>
          <v-tab> Banco de Dados </v-tab>
          <v-tab> Arquivos e FTP </v-tab>
          <v-tab> Aplicativos </v-tab>
          <v-tab> Ferramentas </v-tab>
          <v-tab> Gerenciamento </v-tab>
        </v-tabs>
      </div>
      <div class="painel">
        <img class="img2" src="./assets/Icon.png" alt="icone " />
        <p class="txt2">
          Esse é o nosso novo painel de Hospedagem. Fizemos várias melhorias
          para aperfeiçoar sua experiência com nosso produto. Aproveite!
        </p>
        <img class="img2" src="./assets/seta.png" alt="seta " />
        <img class="img2" src="./assets/x.png" alt="icone de fechar" />
      </div>
      <div class="filtro">
        <div class="btn_input">
          <v-sheet width="300" class="mx-auto">
            <v-form @submit.prevent>
              <v-text-field
                v-model="firstName"
                :rules="rules"
                label="Adicione sua rede"
              ></v-text-field>
            </v-form>
          </v-sheet>
          <v-btn>Filtrar</v-btn>
        </div>
        <v-col cols="auto"> </v-col>
        <div class="add_rede">
          <v-btn variant="outlined" color="red">Adicionar rede </v-btn>
        </div>
      </div>
      <div class="sites">
        <div class="ajuste">
          <img class="img2" src="./assets/Draw.png" alt="seta " />
          <p class="linha"></p>
          <img class="img2" src="./assets/windows.png" alt="seta " />
          <div class="detalhes">
            <p class="exemplo">siteexemplo.com.br</p>
            <div class="usuario">
              <p class="site">site ativo</p>
              <p class="usuario_ex">Usuário FTP: exemplo1</p>
            </div>
          </div>
        </div>
        <v-btn variant="outlined" color="red">Adiministrar</v-btn>
      </div>
      <v-container>
        <v-row justify="center">
          <v-col cols="8">
            <v-container class="max-width">
              <v-pagination
                v-model="page"
                class="my-4"
                :length="15"
              ></v-pagination>
            </v-container>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="footer">
      <img class="img1" src="./assets/Rodapé.png" alt="footer" />
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    rules: [
      (value) => !!value || "Required.",
      (value) => (value || "").length <= 20 || "Max 20 characters",
      (value) => {
        const pattern =
          /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
        return pattern.test(value) || "Invalid e-mail.";
      },
    ],
    data() {
      return {
        page: 1,
      };
    },
  }),
};
</script>


<style>
@import url("https://fonts.googleapis.com/css2?family=Ubuntu&display=swap");
.geral {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  width: 100%;
}
.linha {
  width: 1px;
  height: 41px;
  left: 56px;
  top: 20px;
  background: #d9d9d9;
}
.main {
  width: 1440px;
}
.ma-2 {
  width: 200px;
  height: 30px;
  display: flex;
  justify-content: center;
  font-family: "Ubuntu", sans-serif;
}
.img1 {
  width: 100%;
}
.img2 {
  width: 18px;
  height: 18px;
}
.text-center {
  display: flex;
  justify-content: space-around;
  font-family: "Ubuntu", sans-serif;
  margin-top: 22px;
}
.itens {
  margin-top: 30px;
  display: flex;
  justify-content: space-between;
  width: 200px;
  height: 18px;
  font-family: "Ubuntu", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 150%;
}
.title {
  margin-top: 30px;
  font-family: "Ubuntu";
  font-style: normal;
  font-weight: 500;
  font-size: 34px;
  line-height: 150%;
  color: #424242;
}
.txt {
  font-family: "Ubuntu", sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 150%;
  color: #424242;
}
.painel {
  box-sizing: border-box;
  align-items: flex-start;
  padding: 16px;
  gap: 16px;
  position: absolute;
  width: 1080px;
  height: 80px;
  margin-top: 30px;
  background: #ffffff;
  border-left: 4px solid #43a047;
  box-shadow: 0px 2px 2px rgba(33, 33, 33, 0.25);
  border-radius: 4px;
  font-family: "Ubuntu", sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 150%;
  display: flex;
  align-items: center;
  color: #424242;
}
.filtro {
  display: flex;
  justify-content: space-between;
  width: 1075px;
  margin-top: 160px;
  align-items: center;
}
.sites {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  height: 81px;
  align-items: center;
  width: 1080px;
  padding: 16px;
  background: #ffffff;
  border: 1px solid #eeeeee;
  box-shadow: 0px 2px 2px rgba(33, 33, 33, 0.25);
  border-radius: 8px;
}
.usuario {
  display: flex;
  justify-content: space-around;
}
.ajuste {
  display: flex;
  justify-content: space-around;
  width: 400px;
  align-items: center;
}
.exemplo {
  font-size: 20px;
  font-family: "Ubuntu";
  font-style: normal;
  font-weight: 700;
  line-height: 150%;
  display: flex;
  align-items: center;
  color: #424242;
}
.site {
  font-family: "Ubuntu";
  font-style: normal;
  font-weight: 700;
  font-size: 12px;
  line-height: 150%;
  display: flex;
  color: #43a047;
}
.usuario_ex {
  font-family: "Ubuntu";
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 150%;
  color: #424242;
}
.btn_input {
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 500px;
}
</style>