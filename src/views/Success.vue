<template>
    <div>
        <div class="d-flex success-checkout align-items-center justify-content-center">
            <div class="col col-lg-4 text-center">
                <img src="images/success-buy.png" alt="" width="294">
                <h3 class="mt-4">
                    Sukses Terbayar!
                </h3>
                <p class="mt-2">
                    Silakan tunggu update terbaru dari kami via email yang sudah Anda daftarkan sebelumnya.
                </p>
                <router-link to="/">
                <span class="primary-btn pd-cart mt-3">Back to Home</span>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Success'
}
</script>

<style>

</style>