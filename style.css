let btn = document.querySelectorAll(".btn")
let resetBtn = document.querySelector("#reset");
let newGameButton =  document.querySelector(".newGame");
let msg = document.querySelector(".msg");
let draw = document.querySelector(".draw-msg");
let turnX = true;
let winner = "";

let winPats=[
    [0,1,2],// hor
    [3,4,5],// hor
    [6,7,8],// hor
    [0,3,6],// ver
    [1,4,7],// ver
    [2,5,8],// ver
    [0,4,8],// dia
    [2,4,6],// dia
]
let count = 0;
btn.forEach((btn)=>{

    btn.addEventListener("click", ()=>{
        if(turnX){
            btn.innerText = "X";
            turnX = false;
        } else {
            btn.innerText = "O";
            turnX = true;
        }
        btn.disabled = true;
        count+=1;
        if(checkWinner()){
            btn.disabled = true;
            msg.classList.remove("hide");
            newGameButton.classList.remove("hide");
            msg.innerText =`Congratulations! Winner is ${winner}`;

        }
        if(count===9 && winner=="" ){
            draw.classList.remove("hide");
            newGameButton.classList.remove("hide");
            draw.innerText = "-Match Draw-";
            count = 0;
        }
        winner=""
    })
})

const disableButtons = () =>
{
    for (let btns of btn){
        btns.disabled=true;
    }
}

const checkWinner = () =>{
    for(pat of winPats){
       if (btn[pat[0]].innerText!="" && btn[pat[1]].innerText!="" && btn[pat[2]].innerText!="")
       {
        if(btn[pat[0]].innerText===btn[pat[1]].innerText && btn[pat[1]].innerText===btn[pat[2]].innerText){
            disableButtons();
            winner=btn[pat[1]].innerText ;
            return true;
        }
       }
    }
}

const enableButtons = () =>
{
    for (let btns of btn){
        btns.disabled=false;
        btns.innerText="";
    }
}

const reset = () =>
{
    turnX=true; 
    msg.classList.add("hide");
    enableButtons();
    newGameButton.classList.add("hide");
    draw.classList.add("hide");
    count=0;
};

resetBtn.addEventListener("click",reset);
newGameButton.addEventListener("click",reset);
