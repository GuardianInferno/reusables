<template>
    <div class="container">
        <div class='bird'></div>
    </div>
</template>

<style scoped>
.container{
    width:100vw;
    animation: fly-across 10s linear infinite;
}
.bird{
    background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/174479/bird-cells-new.svg');
    background-size: auto 100%;
    width: 88px;
	height: 125px;
    animation: fly 1s steps(10) infinite;
}

@keyframes fly{
	100% {
		background-position: -900px 0;
	}
}

@keyframes fly-across{
    0%{
        transform: translateY(0vh) translateX(-10vw);
    }
    10%{
        transform: translateY(2vh) translateX(2vw);
    }
    20%{
        transform: translateY(4vh) translateX(14vw);
    }
    30%{
        transform: translateY(2vh) translateX(26vw);
    }
    40%{
        transform: translateY(0vh) translateX(38vw);
    }
    50%{
        transform: translateY(-2vh) translateX(50vw);
    }
    60%{
        transform: translateY(0vh) translateX(62vw);
    }
    70%{
        
        transform: translateY(2vh) translateX(74vw);
    }
    80%{
        transform: translateY(4vh) translateX(86vw);
    }
    90%{
        transform: translateY(2vh) translateX(98vw);
    }
    100%{
        transform: translateY(0vh) translateX(110vw);
    }
}
</style>