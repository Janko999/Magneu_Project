<template>
	<!-- Navbar -->
	<nav class="navbar navbar-dark bg-dark">
		<div class="container justify-content-center align-items-center">
			<a class="navbar-brand " href="#">
				<img :src="page_logo" alt="gamblers know page logo" style="width: 200px;">
			</a>
		</div>
	</nav>

	<!-- Body -->

	<body>
		<section id="main">
			<div class="container-fluid background-image img-fluid">
				<div class="row justify-content-center pt-3">

					<!-- Header Text -->
					<div class="col-10 col-md-4 col-lg-3 col-xl-10 col-xxl-2 text-center mt-2">
						<div>
							<h1 class="header-text" :style="{ color: `${header_text_color}` }">
							{{ header }}
							</h1>
						</div>
					</div>

					<!-- Subheader Text -->
					<div class="row justify-content-center">
						<div class="col-7 col-md-3 col-lg-3 col-xxl-2 text-center text-md-center">
							<h2 class="subheader-text" 
								:style="{ color: `${subheader_text_color}` }">
								{{ subheader }}
							</h2>

							<div class="justify-content-center d-none d-md-block d-flex">
								<hr class="vertical-line" :style="{ borderBottom: `1px solid ${underline_color}` }">
							</div>
						</div>
					</div>

					<!-- Carousel -->
					<section id="fun_box">
						<div id="carouselExampleIndicators" class="carousel slide">
							<div class="carousel-inner">
								<div class="carousel-item active">
									<img src="src\assets\images\casino2.jpg" class="d-block w-100" alt="...">
								</div>
								<div class="carousel-item">
									<img src="src\assets\images\casino6.jpg" class="d-block w-100" alt="...">
								</div>
								<div class="carousel-item">
									<img src="src\assets\images\casino7.png" class="d-block w-100" alt="...">
								</div>
							</div>
							<button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators"
								data-bs-slide="prev">
								<span class="carousel-control-prev-icon" aria-hidden="true"></span>
								<span class="visually-hidden">Previous</span>
							</button>
							<button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators"
								data-bs-slide="next">
								<span class="carousel-control-next-icon" aria-hidden="true"></span>
								<span class="visually-hidden">Next</span>
							</button>
						</div>
					</section>

					<!-- Text under Carousel -->
					<div class="row justify-content-center">
						<div class="col-10 col-lg-4 col-md-4 col-xxl-3 text-center text-md-center">
							<p class="small-text">Add your name and email below to gain instant
								access to our exclusive bonuses</p>
						</div>
					</div>

					<!-- F O R M -->
					<div class="justify-content-center col-11 col-md-5 col-lg-3 text-center ">
						<form>
							<!-- Name input -->

							<div class="form-group ">
								<input type="text" class="form-control" id="name"
								:placeholder ="field_name_text" required pattern="[A-Za-z]+"
									title="Name should only contain letters" autocomplete="off">
								<hr class="vertical-line-form" :style="{ borderBottom: `2px solid ${underline_color}` }">
							</div>
							<!-- E-mail input  -->
							<div class="form-group pt-1">
								<input type="email" class="form-control" id="email" name="name" :placeholder ="field_email_text" autocomplete="off" required >
								<hr class="vertical-line-form" :style="{ borderBottom: `2px solid ${underline_color}` }">
								<div class="invalid-feedback">
									Please enter valid email
								</div>
							</div>

							<!-- Radio Check Buttons -->
							<div class="form-check mt-3 text-start justify-content-center">
								<input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1"
									checked>
								<label class="form-check-label" for="flexRadioDefault1">
									
										I consent to recieve updates about new offers and bonuses via email. 
										Your information will not be shared. You can opt out at any time
									
								</label>
							</div>

							<div class="form-check align-items-center text-start" >
								<input class="form-check-input mt-2" type="radio" name="flexRadioDefault" id="flexRadioDefault2">
								<label class="form-check-label" for="flexRadioDefault2" >
									
										I am over 18 and accept the <a href="#" :style="{ color: `${underline_color}`}" style="text-decoration: none;">Terms & Conditions and Privacy Policy</a>
									
								</label>
							</div>
							<!-- Button -->
							<div class="col-12">
								<button type="submit" class="button"
									:style="{ backgroundColor: `${button_color}` }">{{ button_text }}</button>
							</div>
						</form>
					</div>

				</div>
				<!-- Terms and condition -->
				<div class="row justify-content-center mt-1">
					<div class="col-11 col-md-5 col-lg-4  text-center text-md-center">
						<h5 class="terms1">{{ terms_and_conditions }}</h5>
					</div>
				</div>

			</div>

		</section>
	</body>

	<footer class="footer" >

		<!-- Links -->
		<div class="container">
			<div class="container text-light pt-2">
				<div class="row-auto d-flex flex-row flex-nowrap align-items-center justify-content-center links">
					<div class="col col-md-1 border-right text-nowrap text-center">
						Terms & coditions
					</div>
					<div class="vr"></div>
					<div class="col col-md-1 border-right text-nowrap text-center">
						Privacy Policy
					</div>
					<div class="vr"></div>
					<div class="col col-md-1 border-right text-nowrap text-center">
						Contact Us
					</div>
					<div class="vr"></div>
					<div class="col col-md-1 border-right text-nowrap text-center">
						Unsubscribe
					</div>
					<div class="vr"></div>
					<div class="col col-md-1 border-right text-nowrap text-center border-0">
						Disclaimer
					</div>

				</div>
			</div>

			<!-- Footer Header Text -->
			<div class="container">
				<div class="row justify-content-center mt-3">
					<div class="col-lg-8 col-md-6">
						<div class="text-center">
							<h5 id="responsible" :style="{ color: `${footer_headline_text_color}` }">Responsible Gaming
							</h5>
						</div>
					</div>
				</div>
			</div>

			<!-- Footer Text -->
			<div class="row justify-content-center mt-2">
				<div class="col-lg-6 col-md-6 text-center text-md-center">
					<h5 class="terms mb-3" style="color: aliceblue;">Lorem ipsum dolor sit amet consectetur, adipisicing
						elit. Voluptatem repudiandae dolores reiciendis error accusamus ratione a quia architecto? Quaerat
						perferendis magni quisquam aliquid facilis ea temporibus vel ut quidem obcaecati eum tenetur quis
						atque odit dolore quibusdam exercitationem, adipisci commodi quod placeat. Quisquam beatae commodi
						consequuntur repellat hic, error eum minus dignissimos? Eius, illo reiciendis maxime, inventore
						delectus sed iste sunt quisquam eos dolores exercitationem odit ex esse magni corporis assumenda qui
						omnis debitis labore! Illo veniam quo a porro.</h5>
				</div>
			</div>

			<!-- Footer LOGOS -->
			
				<div class="row justify-content-center align-items-end">

					<div class="col col-md-1 col-lg-1 d-flex text-center justify-content-center align-items-center">
						<a href="#">
							<img :src=logo_1 alt="Logo 1" class="img-fluid image1 mx-auto" />
						</a>
					</div>

					<div class="col col-md-1 col-lg-1 d-flex text-center">
						<a href="#">
							<img :src=logo_2 alt="Logo 2" class="img-fluid image2 mx-auto" />
						</a>
					</div>

					<div class="col col-md-1 col-lg-1 d-flex text-center">
						<a href="#">
							<img :src=logo_3 alt="Logo 3" class="img-fluid image2 mx-auto" />
						</a>
					</div>

					<div class="col col-md-1 col-lg-1 d-flex text-center">
						<a href="#">
							<img :src=logo_4 alt="Logo 4" class="img-fluid image2 mx-auto" />
						</a>
					</div>

					<div class="col col-md-1 col-lg-1 d-flex text-center">
						<a href="#">
							<img :src=logo_5 alt="Logo 5" class="img-fluid  image2 mx-auto" />
						</a>
					</div>

				</div>
			
		</div>

		<div class="container-fluid border-white" :style="{ backgroundColor: `${footer_color}` }">
			<div class="row justify-content-center align-items-center mt-3">
				<div class="col-lg text-center mt-2">
					<h6 class="copy-rights" style="color: black;">&copy; 2023 Gamblers Know | All rights reserved</h6>
				</div>
			</div>
		</div>
	</footer>
</template>


<script>

import axios from 'axios';

export default {
	data() {
		return {
			registration_data: {},
			page_logo: "",
			header: "",
			header_text_color: "",
			subheader_text_color: "",
			subheader:"",
			footer_color: "",
			footer_headline_text_color: "",
			button_color: "",
			button_text:"",
			underline_color: "",
			inputField: "",
			field_name_text: "",
			field_email_text:"",
			terms_and_conditions: "",
			logo_1: "",
			logo_2: "",
			logo_3: "",
			logo_4: "",
			logo_5: "",
			name: "",
			nameRegex: /^[a-zA-z]+$/
		}
	},
	async created() {
		try {
			const response = await axios.get('src/GamblersKnowAPI.json')
			this.registration_data = response.data
			this.page_logo = this.registration_data.page_logo
			this.header = this.registration_data.header
			this.header_text_color = this.registration_data.colors.header_text_color
			this.subheader_text_color = this.registration_data.colors.subheader_text_color
			this.subheader = this.registration_data.subheader
			this.footer_color = this.registration_data.colors.footer_color
			this.footer_headline_text_color = this.registration_data.colors.footer_headline_text_color
			this.button_color = this.registration_data.colors.button_color
			this.button_text = this.registration_data.button_text
			this.terms_and_conditions = this.registration_data.terms_and_conditions
			this.underline_color = this.registration_data.colors.underline_color
			this.field_name_text = this.registration_data.login_fields.field_name_text
			this.field_email_text = this.registration_data.login_fields.field_email_text
			this.logo_1 = this.registration_data.footer_logos.logo_1
			this.logo_2 = this.registration_data.footer_logos.logo_2
			this.logo_3 = this.registration_data.footer_logos.logo_3
			this.logo_4 = this.registration_data.footer_logos.logo_4
			this.logo_5 = this.registration_data.footer_logos.logo_5

		} catch (error) {
			return error
		}
	}
}



</script>

<style scoped>

@font-face {
	font-family: 'Font1';
	src: url('src/assets/fonts/font1/Gilroy-Regular.ttf');
}

@font-face {
	font-family: 'Font2';
	src: url('src/assets/fonts/font2/Montserrat-Medium.ttf');
}

@font-face {
	font-family: 'Font3';
	src: url('src/assets/fonts/font3/Montserrat-SemiBold.ttf');
}


#main {
	color: aliceblue;

}


input {
	color: white;
}



input:focus {
	background-color: transparent;
	color: white;
	box-shadow: none;
}

input:focus::placeholder {
	color: transparent;
}

.vertical-line {
	width: 50%;
	opacity: 100%;
	margin-left: 25%;
	border-top: none;

}

.vertical-line-form {
	opacity: 100%;
	border-top: none;
	margin: 0;
	padding: 0;

}

.button {
	color: rgb(52, 51, 51);
	width: 100%;
	margin-bottom: 10px;
	border: none;
	margin-top: 10px;
	font-weight: bold;
	font-size: 15px;
	padding: 10px;

}

.small-text {
	margin-top: 10px;
	font-family: "Font1";
	font-size: 12px;
	line-height: 1;
}

.header-text {
	font-family: "Font2";
	font-size: 32px;
	line-height: 1;
}

.subheader-text {
	font-family: "Font1";
	font-size: 14px;

}
.vr {
    border-left: 3px solid white;
    height: 5px;
    margin: 0 10px;
	opacity: 0.75;
}

.form-control {
	height: 70%;
	border-left: none;
	border-right: none;
	border-top: none;
	background: transparent;
	box-shadow: none;
	border-bottom: none;

}
.form-control::placeholder {
	text-align: center;
	color: white;

}

.terms1 {
	font-family: "Font2";
	font-size: 7px;
}


.form-check-input[type="radio"] {
	width: 15px;
	height: 15px;
	margin-right: 2px;
	border-radius: 50%;
	background-color: transparent;
	border: 2px solid #46e65a;

}

.form-check-input[type="radio"]:checked {
	background-color: transparent;
	border-color: #46e65a;

}

.form-check-label {
	width: 95%;
	margin-left: 3px;
	font-size: 7px;
	line-height: 1;
}

.terms {
	font-family: "Font2";
	font-size: 8px;

}

.carousel-item img {
	object-fit: cover;
	height: 200px;
}


#submain {
	background-color: black;
	color: aliceblue;
}

.border-right {
	font-size: 7px;
}



.footer {
	background-color: black;
}

.copy-rights {
	font-size: 8px;
}

.image1{
	height: 20px;
}

.image2{
	height: 15px;
	width: 100%;
}


@media (max-width: 426px) {
	.background-image {
		background-image: url('src/assets/images/mobile_bg-image.png');
		background-size: cover;
		background-repeat: no-repeat;
		position: relative;
		background-position: center;

	}
	.vr{
		border-left: 1px solid #46e65a;
		height: 5px;
	}


}


@media (min-width: 427px) {
	.background-image {
		background-image: url('src/assets/images/main_background_image-transformed (1).png');
		background-size: cover;
		height: 100%;
		position: relative;
	}
	.header-text{
		font-size: 30px;
	}
	.carousel{
		display: none;
	}
	.form-check-label {
	width: 95%;
	margin-left: 3px;
	font-size: 8px;
	line-height: 1;
	}

	.small-text {
	margin-top: 1px;
	}

	#responsible{
		font-size: 15px;
	}
	
}



</style>
