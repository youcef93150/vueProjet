<template>
    <header> <h1>S'inscrire</h1></header>

    <div>
        <form @submit.prevent="handleSubmit">
            <div>
                <label for="username">Nom : </label>
                <input
                    id="nom"
                    v-model="nom"
                    type="text"
                    placeholder="Entrez votre nom"
                    required
                />
            </div>
            <div>
                <label for="username">Prénom : </label>
                <input
                    id="prenom"
                    v-model="prenom"
                    type="text"
                    placeholder="Entrez votre prénom"
                    required
                />
            </div>

            <div>
                <label for="email">Email : </label>
                <input
                    id="email"
                    v-model="email"
                    type="email"
                    placeholder="Entrez votre email"
                    required
                />
            </div>

            <div>
                <label for="mdp">Mot de passe : </label>
                <input
                    id="mdp"
                    v-model="mdp"
                    type="password"
                    placeholder="Entrez votre mot de passe"
                    required
                />
            </div>

            <button type="submit">S'inscrire</button>
        </form>
    </div>
</template>

<script>
export default {
  name: 'Register',
  data() {
    return {
      nom: '',
      prenom: '',
      email: '',
      mdp: ''
    };
  },
  methods: {
    handleSubmit() {
      alert(`Nom: ${this.nom}\nPrénom: ${this.prenom}\nEmail: ${this.email}\nMot de passe: ${this.mdp}`);
      // Réinitialiser le formulaire après soumission
      this.nom = '';
      this.prenom = '';
      this.email = '';
      this.mdp = ''; // correction de 'password' en 'mdp'
    }
  }
};
</script>

<style scoped>
header {
    text-align: center;
    margin-bottom: 20px;
}

form {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    background-color: #f9f9f9;
}

div {
    margin-bottom: 15px;
}

label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 16px;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background-color: #0056b3;
}
</style>
