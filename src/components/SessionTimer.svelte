<script>
  let seconds = 0;
  let interval;

  let displaySeconds = 0;
  let displayMinutes = 0;
  let displayHours = 0;


  function startTimer() {
    if (!interval) {
      interval = setInterval(() => {
        seconds++;
      }, 1000)
    }

  }

  function pauseTimer() {
    clearInterval(interval);
    interval = null;
  }

  function resetTimer() {
    pauseTimer();
    console.log(interval)
    seconds = 0;
  }

  function fmtMSS(s){return(s-(s%=60))/60+(9<s?':':':0')+s}




</script>

<div>Session Timer</div>


{fmtMSS(seconds)}
<br>

<button on:click={startTimer}>Start</button>
<button on:click={pauseTimer}>Pause</button>
<button on:click={resetTimer}>Reset</button>
