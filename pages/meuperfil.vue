<script setup>

import '~/assets/css/meuperfil.css'

</script>


<template>

<div class="container">
<div class="row gutters">
	<div class="col-xl-3 col-lg-3 col-md-12 col-sm-12 col-12 ajuste">
		<div class="cardp h-100">
			<div class="card-body ">
				<div class="account-settings">
					<div class="user-profile">
						<div class="user-avatar">
							<img src="/public/baixados.png" alt="Maxwell Admin">
						</div>
						<h5 class="nomeuser ">Sophia Hardwell</h5>
						<h6 class="user-email">SophiaHardwell@gmail.com</h6>
					</div>
					<div class="about ">
						<h5 class="mb-2 text-primary textocardcl">Sobre mim:</h5>
						<p>Sou uma mulher apaixonada pela vida e em constante busca de crescimento e aprendizado.</p>
					</div>
				</div>
			</div>
		</div>
	</div>
	<div class="col-xl-9 col-lg-9 col-md-12 col-sm-12 col-12 ">
		<div class="card2p h-100">
			<div class="card-body">
				<div class="row gutters">
					<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12 ">
						<h6 class="mb-3 text-primary textocard2 ajusteusercf ">Informações Pessoais</h6>
					</div>
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12">
						<div class="form-group textocardcl ajusteusercf aaajuste2">
							<label for="fullName">Nome Completo</label>
							<input type="text" class="form-control placeh" id="fullName" placeholder="Nome Completo:">
						</div>
					</div>
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12 ">
						<div class="form-group textocardcl ajusteusercf">
							<label for="eMail">Email</label>
							<input type="email" class="form-control placeh" id="eMail" placeholder="Email:">
						</div>
					</div>
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12">
						<div class="form-group textocardcl ajusteusercf">
							<label for="phone">Senha</label>
							<input type="text" class="form-control placeh" id="phone" placeholder="Senha:">
						</div>
					</div>
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12">
						<div class="form-group textocardcl ajusteusercf">
							<label for="website">Data de Nascimento</label>
							<input type="url" class="form-control placeh" id="website" placeholder="Data de Nascimento:">
						</div>
					</div>
				</div>
				<div class="row gutters">
					<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
						<h6 class="mb-3 text-primary textocard2 ajusteusercf ajustetminfo aaajuste">Endereço:</h6>
					</div>
					
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12">
						<div class="form-group textocardcl ajusteusercf">
							<label for="ciTy">Cidade</label>
							<input type="name" class="form-control placeh" id="ciTy" placeholder="Sua Cidade:">
						</div>
					</div>
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12">
						<div class="form-group textocardcl ajusteusercf">
							<label for="sTate">Estado</label>
							<input type="text" class="form-control placeh" id="sTate" placeholder="Seu Estado">
						</div>
					</div>
					<div class="col-xl-6 col-lg-6 col-md-6 col-sm-6 col-12">
						<div class="form-group textocardcl ajusteusercf">
							<label for="zIp">CEP</label>
							<input type="text" class="form-control placeh" id="zIp" placeholder="CEP">
						</div>
					</div>
				</div>
				<div class="row gutters">
					<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
						<div class="text-right">
							<button type="button" id="submit" name="submit" class="btnf btn-secondary">Cancelar</button>
							<button type="button" id="submit" name="submit" class="btnf btn-primary">Atualizar</button>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
</div>

</template>