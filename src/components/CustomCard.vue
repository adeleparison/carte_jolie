<template>
    <div class="page">
        <div class="preview">
            <!-- On lie "preview" avec les inputs-->
            <p> {{ preview.title }} </p>
            <p> {{ preview.text }} </p>
            <p> {{ preview.expe }} </p>
        </div>
        <form class="customisation">
            <div class="theme-checkboxes">
				<h3>Choisissez un thème :</h3>
				<select>
                    <!-- On utilise une boucle for pour récuperer les differents thèmes-->
					<option v-for="theme in themes">{{ theme }}</option>
				</select>
			</div>
            <div class="text">
                <!-- v-model permet de lier la premiere div avec les inputs-->
				<input v-model="preview.title" type="text" placeholder="Entrez le titre de votre carte">
				<div class="icons">
					<i class="fa fa-font" aria-hidden="true"></i>
					<i class="fa fa-align-justify" aria-hidden="true"></i>
					<i class="fa fa-align-center" aria-hidden="true"></i>
					<i class="fa fa-align-right" aria-hidden="true"></i>
					<i class="fa fa-align-left" aria-hidden="true"></i>
				</div>
				<textarea v-model="preview.text" cols="35" rows="5" placeholder="Veuillez entrer votre message personnalisé"></textarea>
				<div class="icons">
					<i class="fa fa-font" aria-hidden="true"></i>
					<i class="fa fa-align-justify" aria-hidden="true"></i>
					<i class="fa fa-align-center" aria-hidden="true"></i>
					<i class="fa fa-align-right" aria-hidden="true"></i>
					<i class="fa fa-align-left" aria-hidden="true"></i>
				</div>
			</div>
            <div class="names">
				<input v-model="preview.expe" type="text" placeholder="Expéditeur de la carte" />
			</div>
            <div class="anim-checkboxes">
                <h3>Choisissez une animation :</h3>
                <input type="checkbox">
                <label>Bounce</label>
                <input type="checkbox">
                <label>Shuffle</label>
                <input type="checkbox">
                <label>Show</label>
                <input type="checkbox">
                <label>Width</label>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
       data() {
           return {
               preview: {
                   //variable = valeur
                   theme:'',
                   title:'',
                   text:'',
                   expe:'',
                   anim:'',
                   
               },
               
               themes : ['Noël', 'Mariage', 'Anniversaire', 'Nouvel An', 'Naissance'],
           }
       } 
    }
</script>

<style>
    .page {
        display: flex;
        
    }
    .preview {
        border: 1px solid black;
    }
</style>