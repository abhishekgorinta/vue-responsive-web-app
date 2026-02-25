<template>
    <div class="footer-bottom">
        <p>© <span>2026</span> ABHI. All rights reserved.
            <span class="br">| Follow us on
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
            </span>
        </p>
    </div>
</template>

< <style scoped>
.footer-bottom {
    background-color: #282C3F;
    border-top: 1px solid rgba(255, 255, 255, 0.04);
    margin-top: 24px;
    padding-top: 12px;
    text-align: center;
    color: grey;
    font-size: 13px;
    height: 50px;
}

.footer-bottom a {
    color: grey;
    margin-left: 8px;
    text-decoration: none;
    border: 1px solid grey;
    border-radius: 100%;
    padding: 5px;
}

.footer-bottom a:hover {
    color: #E4272C;
}

@media (max-width:600px) {
    .footer-bottom {
        background-color: #282C3F;
        border-top: 1px solid rgba(255, 255, 255, 0.04);
        margin-top: 24px;
        padding-top: 12px;
        text-align: center;
        color: grey;
        font-size: 13px;
        height: 100px;
    }

    .footer-bottom a {
        color: grey;
        margin-left: 8px;
        text-decoration: none;
        border: 1px solid grey;
        border-radius: 100%;
        padding: 5px;
        height: 100px;
    }

    .footer-bottom a:hover {
        color: #E4272C;
    }

    .br {
        margin-top: 20px;
        display: block;
    }
}
</style>