<template>
    <b-navbar toggleable="lg" type="dark" variant="dark">
        <b-navbar-brand href="https://zerocodenft.com">
            Zero Code NFT
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
                <b-nav-item to="/#roadmap">Roadmap</b-nav-item>
                <b-nav-item to="/#team">Team</b-nav-item>
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-button
                    variant="light"
                    :disabled="!!$wallet.account"
                    @click="$wallet.connect">
                    <strong>{{
                        !!$wallet.account ? $wallet.accountCompact : 'Connect Wallet'
                    }}</strong>
                </b-button>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
</template>