<template>
    <section class="my-32">
        <h2>Me Contacter</h2>

        <!--mise en ligne des élements (formulaire + réseaux) en ligne-->
        <div class="lg:flex flex-row-reverse">

            <!-- comportement des 2 bloques des réseaux -->
            <div class="mx-5 my-8 md:mx-14 md:my-16 xl:mx-28 flex md:block flex-wrap justify-between gap-5">
    
                <!-- sticky -->
                <div class="sticky top-1/3">

                    <!-- bloque linkedin + insta-->
                    <div class=" my-8 w-full max-w-2xl flex flex-wrap flex-row justify-between lg:flex-col gap-5 md:gap-8 ">

                        <a target="_blank" href="https://www.linkedin.com/in/aurélie-runser-10a763224">
            
                            <linkedinIcon class="inline-block w-7 h-7 md:w-10 md:h-10"/>
                            <p class="sr-only">Mon compte Linkedin : </p>
                            <p class="contact_link inline-block ml-3 w-auto font-darker-grotesque font-bold text-base md:text-lg text-orange-100 underline decoration-fuchsia-500">
                                /in/aurélie-runser-10a763224
                            </p>
            
                        </a>
            
                        <a target="_blank" href="https://www.instagram.com/aurelie.projetmmi/">
            
                            <instagramIcon class="inline-block w-7 h-7 md:w-10 md:h-10"/>
                            <p class="sr-only">Mon compte Instagram : </p>
                            <p class="contact_link inline-block ml-3 w-auto font-darker-grotesque font-bold text-base md:text-lg text-orange-100 underline decoration-fuchsia-500">
                                @aurelie.projetmmi
                            </p>
            
                        </a>

                    </div>
        
                    <!-- bloque mail + phone -->
                    <div class=" md:my-8 w-full max-w-2xl flex flex-wrap flex-row justify-between lg:flex-col gap-5 md:gap-8 ">
                        <a href="mailto:aurelie.runser25@gmail.com">
            
                            <mailIcon class="inline-block w-9 h-9 md:w-12 md:h-12"/>
                            <p class="sr-only">Mon Adresse Mail : </p>
                            <p class="contact_link inline-block ml-3 w-auto font-darker-grotesque font-bold text-base md:text-lg text-orange-100 underline decoration-fuchsia-500">
                                aurelie.runser25@gmail.com
                            </p>
            
                        </a>
            
                        <a href="tel:+33771722003">
            
                            <phonIcon class="inline-block w-9 h-9 md:w-12 md:h-12"/>
                            <p class="sr-only">Mon Numéro de Téléphone : </p>
                            <p class="contact_link inline-block ml-3 w-auto font-darker-grotesque font-bold text-base md:text-lg text-orange-100 underline decoration-fuchsia-500">
                                +33 7 71 72 20 03
                            </p>
            
                        </a>
                    </div>
        
                </div>
            </div>
            
            <!-- formulaire-->
            <div class="grow">
                <form action="https://api.web3forms.com/submit" method="POST" ref="contactForm"
                    class="mx-5 my-14 md:mx-14 md:my-20 md:max-w-2xl xl:mx-28">
        
        
                    <input type="hidden" name="access_key" value="b3a5c0b1-dcc2-48e8-90e1-8ce766ba6253">
        
                    <div class="relative my-16">
                        <input type="text" name="name" placeholder=" " required
                                class="border-2 border-orange-100 p-2 md:p-5">
                        <p class="form_text absolute top-1/2 left-3 -translate-y-1/2
                                font-darker-grotesque font-medium  text-orange-100 opacity-70">
                            Prénom & Nom
                        </p>
        
                        <div class="form_obligatoire p-3 md:p-5">
                            <p class="font-darker-grotesque font-bold text-sm 
                                        md:text-base">* Obligatoire</p>
                        </div>
                    </div>
        
                    <div class="relative my-16">
                        <input type="email" name="email" placeholder=" " required
                                class="border-2 border-orange-100 p-2 md:p-5">
                        <p class="form_text absolute top-1/2 left-3 -translate-y-1/2
                                font-darker-grotesque font-medium  text-orange-100 opacity-70">
                            Adresse Mail
                        </p>
        
                        <div class="form_obligatoire p-3 md:p-5">
                            <p class="font-darker-grotesque font-bold text-sm 
                                        md:text-base">* Obligatoire</p>
                        </div>
                    </div>
                    
                    <div class="relative my-16">
                        <input type="text" name="sujet" placeholder=" " required
                                class="border-2 border-orange-100 p-2 md:p-5">
                        <p class="form_text absolute top-1/2 left-3 -translate-y-1/2
                                font-darker-grotesque font-medium  text-orange-100 opacity-70">
                            Sujet
                        </p>
        
                        <div class="form_obligatoire p-3 md:p-5">
                            <p class="font-darker-grotesque font-bold text-sm 
                                        md:text-base">* Obligatoire</p>
                        </div>
                    </div>
        
                    <div class="relative my-16">
                        <textarea name="message" rows="5" placeholder=" " required
                        class="border-2 border-orange-100 p-2 md:p-5"></textarea>
                        <p class="form_text absolute top-2 left-3
                                font-darker-grotesque font-medium text-lg text-orange-100 opacity-70
                                md:text-xl">
                            Message
                        </p>
        
                        <div class="form_obligatoire p-3 md:p-5">
                            <p class="font-darker-grotesque font-bold text-sm 
                                        md:text-base">* Obligatoire</p>
                        </div>
                    </div>
        
                    <!-- <input type="hidden" name="redirect" value="https://web3forms.com/success"> -->
        
                    <monBouton type="submit" class="mx-auto">
                        Envoyer
                    </monBouton>
        
                </form>
        
                <p v-if="messageSent"
                    class="form_messageSent relative mx-auto w-fit font-oswald font-bold text-lg xl:text-xl text-center text-stone-300">
                    Merci beaucoup, votre message a bien été envoyé !
                </p>
            </div>
        </div>

    </section>
</template>


<style>

/* animation du underline */
.contact_link:hover{
    animation: underline_color 0.5s linear infinite;
}

@keyframes underline_color {
    from{text-decoration-color: #22d3ee;}
    to{text-decoration-color: #d946ef;}
}

/* nécessaire pour que l'utilisateur puisse pas cliquer sur les textes en absolute */
.form_text,
.form_obligatoire {
    pointer-events: none;
    transition: all 0.1s ease-in-out;
}

/* taille du texte mobile sur portable */
.form_text{
    font-size: 1.5rem;
}

/* taille du texte mobile sur moyennet grand écran */
@media screen and (min-width: 768px) {
    .form_text {
        font-size: 2rem;
  }
}

/* style lorsque le texte mobile se déplace sur portable */
input:focus + .form_text,
input:not(:placeholder-shown) ~ .form_text {
    top: -45%;
    font-size: 1rem;
    transition: all 0.1s ease-in-out;
}

textarea:focus + .form_text,
textarea:valid + .form_text{
    top: -20%;
    font-size: 1rem;
    transition: all 0.1s ease-in-out;
}

/* style lorsque le texte mobile se déplace sur moyen et grand écran */
@media screen and (min-width: 768px) {
    input:focus + .form_text,
    input:not(:placeholder-shown) ~ .form_text {
        top: -40%;
        font-size: 1.5rem;
        transition: all 0.1s ease-in-out;
    }

    textarea:focus + .form_text,
    textarea:valid + .form_text{
        top: -20%;
        font-size: 1.5rem;
        transition: all 0.1s ease-in-out;
    }
}


/* style du texte "* Obligatoire" */
.form_obligatoire{
    position: absolute;
    top: 0;
    right: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    padding: 0 10px;

    opacity: 0;
    transition: opacity 0.1s ease-in-out;
}

/* couleur du texte "* Obligatoire" */
.form_obligatoire p{
    color: #d946ef;
}

/* style du texte "*Obligatoire" lorsque l'input n'est pas complete */
input:invalid ~ .form_obligatoire,
textarea:invalid ~ .form_obligatoire{
    opacity: 1;
    transition: opacity 0.1s ease-in-out;
}


/* style autour du message de confirmation de l'envoie du formulaire */
.form_messageSent::before{
    content: "";
    position: absolute;
    top: -15%;
    left: -3%;
    display: block;
    width: 104%;
    height: 120%;
    border: 2px solid #22d3ee;
}
.form_messageSent::after{
    content: "";
    position: absolute;
    bottom: -15%;
    right : -3%;
    display: block;
    width: 104%;
    height: 120%;
    border: 2px solid #d946ef;
}

</style>


<script>
import monBouton from "@/components/monBouton.vue"
import linkedinIcon from "@/components/icons/linkedinIcon.vue"
import instagramIcon from "@/components/icons/instagramIcon.vue"
import mailIcon from "@/components/icons/mailIcon.vue"
import phonIcon from "@/components/icons/phonIcon.vue"

export default {
  name: 'ContactForm',
  components: {monBouton, linkedinIcon, instagramIcon, mailIcon, phonIcon},

  data() {
    return {
      messageSent: false
    }
  },

  mounted(){
        this.$refs.contactForm.addEventListener('submit', this.submitForm)
  },

  methods: {
    async submitForm(event) {
      event.preventDefault()
      const formData = new FormData(event.target)
      const response = await fetch('https://api.web3forms.com/submit', {
        method: 'POST',
        body: formData
      })
      if (response.ok) {
        this.messageSent = true
        // Réinitialiser les champs du formulaire
        const inputs = event.target.querySelectorAll('input, textarea')
        inputs.forEach(input => input.value = '')
      }
    }
  }
}

</script>