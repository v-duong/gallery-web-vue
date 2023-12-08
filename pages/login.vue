<script setup>
    import '~/assets/css/login.css';

    const supabase = useSupabaseClient();

    const loginEmail = ref('');
    const loginPassword = ref('');

    const onClickLogin = async() => {
        try {
            const {data, error} = await supabase.auth.signInWithPassword({
                email: loginEmail.value, 
                password: loginPassword.value
            });
            if (error) throw error;
            console.log(data);
            return navigateTo('/');
        } catch (error) {
            alert(error.error_description || error.message);
        } 
    };
</script>

<template>
    <div class="main-container">
        <h1>Login</h1>
        <form class="form-container">
            <input v-model="loginEmail" type="email" placeholder="Email" >
            <input v-model="loginPassword" type="password" placeholder="Password" >
            <input type="submit" @click.prevent="onClickLogin">
        </form>
    </div>
</template>