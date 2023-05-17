<template>
    <div class="game">
          <div class="crossword">
              <div class="cell cell-1-6"><span>1</span><input class="single-input input_1_6" type="text" maxlength="1"/></div>
              <div class="cell cell-2-6"><input class="single-input input_2_6" type="text" maxlength="1"/></div>
              <div class="cell cell-3-6"><input class="single-input input_3_6" type="text" maxlength="1"/></div>
              <div class="cell cell-4-6"><input class="single-input input_4_6" type="text" maxlength="1"/></div>
              <div class="cell cell-5-6"><input class="single-input input_5_6" type="text" maxlength="1"/></div>
              <div class="cell cell-6-6"><input class="single-input input_6_6" type="text" maxlength="1"/></div>
              <div class="cell cell-7-6"><input class="single-input input_7_6" type="text" maxlength="1"/></div>
              <div class="cell cell-8-6"><input class="single-input input_8_6" type="text" maxlength="1"/></div>



              <div class="cell cell-2-1"><span>2</span><input class="single-input input_2_1" type="text" maxlength="1"/></div>
              <div class="cell cell-2-2"><input class="single-input input_2_2" type="text" maxlength="1"/></div>
              <div class="cell cell-2-3"><input class="single-input input_2_3" type="text" maxlength="1"/></div>
              <div class="cell cell-2-4"><input class="single-input input_2_4" type="text" maxlength="1"/></div>
              <div class="cell cell-2-5"><input class="single-input input_2_5" type="text" maxlength="1"/></div>
              <div class="cell cell-2-7"><input class="single-input input_2_7" type="text" maxlength="1"/></div>
              <div class="cell cell-2-8"><input class="single-input input_2_8" type="text" maxlength="1"/></div>



              <div class="cell cell-6-3"><span>3</span><input class="single-input input_6_3" type="text" maxlength="1"/></div>
              <div class="cell cell-6-4"><input class="single-input input_6_4" type="text" maxlength="1"/></div>
              <div class="cell cell-6-5"><input class="single-input input_6_5" type="text" maxlength="1"/></div>
              <div class="cell cell-6-7"><input class="single-input input_6_7" type="text" maxlength="1"/></div>
              <div class="cell cell-6-8"><input class="single-input input_6_8" type="text" maxlength="1"/></div>
          </div>

        <div class="hints">
            <div>
                <h2>Down :</h2>
                <div>1. Your Special Event</div>
            </div>
            <div>
                <h2>Across :</h2>
                <div>2. Him</div>
                <div>3. Her</div>
            </div>
        </div>
    </div>

    <br/><br/><br/>
    <div class="unlockButton">
        <input class="unlock" type="button" @click="unlockClicked" value="Unlock" />
    </div>

    <div class="bz4X">
    </div>
</template>

<script setup>
function unlockClicked() {
    let down_1 = "";
    let across_2 = "";
    let across_3 = "";

    for (let i=1; i<=8;i++) {
        down_1 += document.getElementsByClassName("input_" + i + "_6")[0].value;
    }

    for (let i=1; i<=8;i++) {
        across_2 += document.getElementsByClassName("input_2_" + i)[0].value;
    }

    for (let i=3; i<=8;i++) {
        across_3 += document.getElementsByClassName("input_6_" + i)[0].value;
    }

    if (down_1.toLowerCase() === "marriage"
        && across_2.toLowerCase() === "abhilash"
        && across_3.toLowerCase() === "ketaki") {
        let game = document.getElementsByClassName("game")[0];
        let unlockButton = document.getElementsByClassName("unlockButton")[0];

        game.innerHTML = "";
        unlockButton.innerHTML = "";

        let video = document.getElementsByClassName("bz4X")[0];
        video.innerHTML = "<iframe src=\"https://drive.google.com/file/d/1hZPmBYD0iRCtW9mZWvoS3VWFREUYPAZr/preview?vq=hd1080\" frameborder=\"0\" width=\"1080\" height=\"680\" allowfullscreen></iframe>" +
            "<p>* Please select 1080p for best experience</p>";
        } else {
            let video = document.getElementsByClassName("bz4X")[0];
            video.innerHTML = "<p style='color: red;'>Try Again</p>"
        }


}

</script>

<style scoped>

.game {
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.crossword {
    display: inline-grid;
    grid-template-rows: repeat(8, 60px);
    grid-template-columns: repeat(8, 60px);
    row-gap: 1px;
    column-gap: 1px;
}

.cell {
    border: 1px solid black;
    display: grid;
    align-items: center;
    justify-items: center;
    position: relative;
}

.cell span {
    font-size: 14px;
    position: absolute;
    top: 0;
    left: 2px;
    background-color: black;
    color: white;
}

.single-input {
    padding: 0;
    width: 40px;
    height: 40px;
    text-align: center;
    font-size: 20px;
    border: 0;
}

.single-input:focus-visible {
    outline: none;
}
.unlockButton {
    text-align: center;
}
.unlock {
    background-color: lightpink;
    color: snow;
    border: 0;
    border-radius: 5px;
    font-size: 16px;
    padding: 20px;
}
.unlock:hover {
    background-color: hotpink;
    cursor: pointer;
}
.bz4X {
    text-align: center;
}

.cell-1-6 { grid-area: 1 / 6;}
.cell-2-6 { grid-area: 2 / 6;}
.cell-3-6 { grid-area: 3 / 6;}
.cell-4-6 { grid-area: 4 / 6;}
.cell-5-6 { grid-area: 5 / 6;}
.cell-6-6 { grid-area: 6 / 6;}
.cell-7-6 { grid-area: 7 / 6;}
.cell-8-6 { grid-area: 8 / 6;}

.cell-2-1 { grid-area: 2 / 1;}
.cell-2-2 { grid-area: 2 / 2;}
.cell-2-3 { grid-area: 2 / 3;}
.cell-2-4 { grid-area: 2 / 4;}
.cell-2-5 { grid-area: 2 / 5;}
.cell-2-7 { grid-area: 2 / 7;}
.cell-2-8 { grid-area: 2 / 8;}

.cell-6-3 { grid-area: 6 / 3;}
.cell-6-4 { grid-area: 6 / 4;}
.cell-6-5 { grid-area: 6 / 5;}
.cell-6-7 { grid-area: 6 / 7;}
.cell-6-8 { grid-area: 6 / 8;}
</style>