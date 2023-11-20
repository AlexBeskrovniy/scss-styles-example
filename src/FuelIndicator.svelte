<style lang="scss">
   @import url('https://fonts.googleapis.com/css?family=IBM+Plex+Sans:400,700&display=swap');
    

.label {
    cursor: pointer;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    #indicator-check {
        display: none;

        &:checked + div {
            margin-left: 100px;
        }
    }
    
    &:hover
        & .toggle-container {
            box-shadow: 0px 0px 15px -3px rgba(200, 200, 200, 0.6), inset 0px 0px 18px 5px rgba(0, 0, 0, 0.75)
        }

    .text {
        text-align: center;
        margin-top: 10px;
        color: #7d7d7d;

        p {
            font-size: 14px;
        }
    }   
}
    
            

.toggle-container {
    width: 260px;
    height: 120px;
    box-shadow: 0px 0px 27px -3px rgba(0, 0, 0, 0.75), inset 0px 0px 18px 5px rgba(0, 0, 0, 0.75);
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;

    &-inner {
        box-shadow: inset 0px 0px 70px 15px rgba(0, 0, 0, 0.5);
        background-color: #101010;
        width: 240px;
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;

        &-ticks {
            box-shadow: inset 0px 0px 20px 10px rgba(0, 0, 0, 0.75), inset 0px 25px 26px -26px rgba(236, 236, 236, 0.5);
            background-color: #080808;
            display: flex;
            padding: 10px 30px;
            position: relative;

            &-cover {
                position: absolute;
                display: flex;
                top: 0;
                left: 0;
                bottom: 0;
                right: 0;
                background-color: rgba(255, 255, 255, 0.05);
            }

            &-container {
                display: flex;

                .tick {
                    color: white;
                    width: 10px;

                    &::after {
                        content: ' ';
                        display: block;
                        margin-left: auto;
                        margin-right: auto;
                        margin-top: 25px;
                        width: 2px;
                        height: 10px;
                        background: #8B8B8B;
                        position: absolute;
                    }
                        
                    &.big {
                        text-align: center;
                        font-size: 12px;
                        font-weight: bold;
                        
                        &::after {
                            height: 15px;
                            margin-top: 10px;
                        }
                            
                        small {
                            font-size: 8px;
                            font-weight: normal;
                        }
                    }
                            
                    &.e {
                        color: #CB3A3A;
                    }
                    &.f {
                        color: #03c703;
                    }
                }
            }       

            &-indicator {
                width: 10px;
                display: block;
                top: 0;
                bottom: 0;
                position: absolute;
                margin-left: 0px;
                transition: all 1.8s ease;
                background-color: rgba(250, 22, 22, 0.3);
            }
        }
    }
}
    
</style>

<label for="indicator-check" class="label">
	<div class="toggle-container">
		<div class="toggle-container-inner">
			<div class="toggle-container-inner-ticks">
				<div class="toggle-container-inner-ticks-cover"></div>
				<div class="toggle-container-inner-ticks-container">
					<div class="tick big e">E</div>
					<div class="tick"></div>
					<div class="tick"></div>
					<div class="tick"></div>
					<div class="tick"></div>
					<div class="tick big m">
						<small>1</small>/<small>2</small>
					</div>
					<div class="tick"></div>
					<div class="tick"></div>
					<div class="tick"></div>
					<div class="tick"></div>
					<div class="tick big f">F</div>
				</div>

				<input type="checkbox" id="indicator-check">
				<div class="toggle-container-inner-ticks-indicator"></div>
			</div>
		</div>
	</div>

	<div class="text">
		<h5>Pure CSS Fuel Gauge Toggle</h5>
		<p>click on the gauge to toggle the indicator</p>
	</div>
</label>