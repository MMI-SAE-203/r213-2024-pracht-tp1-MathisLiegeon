<template>
    <p>hello</p>
    <h1>Titanfall II</h1>
    
    <div class="carrousel" x-data="{hrefCourant: '#ecran-1'}">
        <button 
        @pointerdown="$refs.parent.scrollLeft -= $refs.parent.clientWidth"
        class="carrousel_btn carrousel_btn-avant" aria-label="slide précedant">◁</button>
        <button 
        @pointerdown="$refs.parent.scrollLeft += $refs.parent.clientWidth"
        class="carrousel_btn carrousel_btn-apres" aria-label="slide suivant">▷</button>
        <div 
        class="carrousel_parent-ecrans"
        x-ref="parent"
        @scroll.debounce.250ms.passive="hrefCourant = '#'+ [...$refs.parent.children].find(e=>e.getBoundingClientRect().x>=0).id"
        >
            <div id="ecran-1" class="carrousel_ecran">
                <figure>
                    <!--src="https://picsum.photos/seed/1/500/300"-->
                    <img class="carrousel_ecran-img" src="/public/img/img_1.jpg" alt="image ecran 1">
                    <figcaption>MOONFALL</figcaption>
                </figure>
            </div>
            <div id="ecran-2" class="carrousel_ecran">
                <figure>
                    <img class="carrousel_ecran-img" src="/public/img/img_2.jpg" alt="image ecran 2">
                    <figcaption>RONIN</figcaption>
                </figure>
            </div>
            <div id="ecran-3" class="carrousel_ecran">
                <figure>
                    <img class="carrousel_ecran-img" src="/public/img/img_3.jpg" alt="image ecran 3">
                    <figcaption>PILOTS & MACHINES</figcaption>
                </figure>
            </div>
            <div id="ecran-4" class="carrousel_ecran">
                <figure>
                    <img class="carrousel_ecran-img" src="/public/img/img_4.jpg" alt="image ecran 4">
                    <figcaption>TITAN vs TITAN</figcaption>
                </figure>
            </div>
            <div id="ecran-5" class="carrousel_ecran">
                <figure>
                    <img class="carrousel_ecran-img" src="/public/img/img_5.jpg" alt="image ecran 5">
                    <figcaption>WRAITH</figcaption>
                </figure>
            </div>
        </div>
        <ul class="caroussel_liste-liens">
            <li><a href="#ecran-1" class="caroussel_lien"
                :class="{actif:hrefCourant==='#ecran-1'}"
                >Ecran 1</a></li>
            <li><a href="#ecran-2" class="caroussel_lien"
                :class="{actif:hrefCourant==='#ecran-2'}"
                >Ecran 2</a></li>
            <li><a href="#ecran-3" class="caroussel_lien"
                :class="{actif:hrefCourant==='#ecran-3'}"
                >Ecran 3</a></li>
            <li><a href="#ecran-4" class="caroussel_lien"
                :class="{actif:hrefCourant==='#ecran-4'}"
                >Ecran 4</a></li>
            <li><a href="#ecran-5" class="caroussel_lien"
                :class="{actif:hrefCourant==='#ecran-5'}"
                >Ecran 5</a></li>
        </ul>
    </div>
</template>