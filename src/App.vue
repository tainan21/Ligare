<template>
		<div class="hidden" style="margin-bottom: 60px;">
			<vs-navbar shadow square center-collapsed v-model="active">
				<template #left>
					<vs-button @click="activeSidebar = !activeSidebar" flat icon>
						<i class='bx bx-menu-alt-right'></i>
					</vs-button>						
				</template>
				<template #right>
					<vs-button gradient style="min-width: 60px" success animation-type="scale" to="/Receitas">
						<i class='bx bx-food-menu' ></i>
						<template #animate >Receitas</template>
					</vs-button>
					<vs-button gradient style="min-width: 60px" danger animation-type="scale" to="/MarketPlace">
						<i class='bx bxs-shopping-bag' ></i>
						<template #animate >Surprise</template>
					</vs-button>
					<vs-button gradient style="min-width: 60px" warn animation-type="scale">
						<i class='bx bxs-bell' ></i>
						<template #animate >18</template>
					</vs-button>
<!--					<vs-avatar warn badge badge-color="success">
						<i class='bx bxs-bell' ></i>
						<template #badge>28</template>
					</vs-avatar> -->
					<vs-avatar badge badge-color="success" badge-position="bottom-left" style="margin: 5px 10px;">
						<img src="@/assets/avatar-laysla.jpg" alt="">
					</vs-avatar> 
				</template>
			</vs-navbar>
			<vs-sidebar absolute v-model="active" :open.sync="activeSidebar">
				<template #logo>Ligare</template>
				<vs-sidebar-item id="home" to="/">
					<template #icon><i class='bx bx-home'></i></template>Home
				</vs-sidebar-item>
				<vs-sidebar-item id="about" to="/about">
					<template #icon><i class='bx bx-home'></i></template>Sobre
				</vs-sidebar-item>
				<vs-sidebar-item id="guiaRapido" to="/GuiaRapido">
					<template #icon><i class='bx bx-food-menu'></i></template>Guia Rápido
				</vs-sidebar-item>
				<vs-sidebar-item id="Login" to="/LoginRegister">
					<template #icon><i class='bx bx-home'></i></template>Login
				</vs-sidebar-item>
				<vs-sidebar-item id="Financeiro" to="/FinanceiroControle">
					<template #icon><i class='bx bx-home'></i></template>Finanças
				</vs-sidebar-item>
				<vs-sidebar-item id="market" to="/CrudProdutos">
					<template #icon><i class='bx bx-pie-chart-alt-2'></i></template>Obras
				</vs-sidebar-item>
				<vs-sidebar-group>
					<template #header>
						<vs-sidebar-item arrow>
							<template #icon><i class='bx bx-group'></i></template>Cadastros
						</vs-sidebar-item>
					</template>
					<vs-sidebar-item id="Instagram" to="/Category">
						<template #icon><i class='bx bxl-instagram'></i></template>Obras
					</vs-sidebar-item>
					<vs-sidebar-item id="twitter" to="/Adcionais">
						<template #icon><i class='bx bxl-twitter' ></i></template>Clientes
					</vs-sidebar-item>
					<vs-sidebar-item id="twitter" to="/CrudProdutos">
						<template #icon><i class='bx bxl-twitter' ></i></template>Coolaboradores
					</vs-sidebar-item>
				</vs-sidebar-group>
				<vs-sidebar-group>
					<template #header>
						<vs-sidebar-item arrow>
							<template #icon><i class='bx bx-group'></i></template>Relatórios
						</vs-sidebar-item>
					</template>
					<vs-sidebar-item id="Instagram" to="/">
						<template #icon><i class='bx bxl-instagram'></i></template>Relatório de obra
					</vs-sidebar-item>
					<vs-sidebar-item id="twitter" to="/CrudProdutos">
						<template #icon><i class='bx bxl-twitter' ></i></template>Relatório de Desempenho
					</vs-sidebar-item>
					<vs-sidebar-item id="Facebook" to="/">
						<template #icon><i class='bx bxl-facebook' ></i></template>Relatório de Custos
					</vs-sidebar-item>
				</vs-sidebar-group>
			</vs-sidebar>
      <menuBottom />
		</div>
	</template>
<script>
import menuBottom from '@/components/menuBottom.vue'

	export default {
      components: {
      'menuBottom': menuBottom,
      },
		data:() => ({
			active: 'home',
			activeSidebar: false
		})
	}
	</script>

<style>
 @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600;700&display=swap');
 @import url('https://unpkg.com/boxicons@2.0.7/css/boxicons.min.css');
 </style>