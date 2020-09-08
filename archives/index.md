---
title: 
layout: page 
---


<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<link rel = "stylesheet"
   type = "text/css"
   href = "style.css" />
</head>

<style>

#test p {
  opacity: 0;
}
</style>

<script>
$("#test p").delay(10).animate({ opacity: 1  }, 700);
</script>


<div class="row">
  <div class="column">
    <div class="card">
      <img src="/archives/Images/pear.svg" alt="PEAR" id="project">
      <div class="container">
        <h2>Pear</h2>
        <p class="title">Decentralized Journal</p>
        <p>Smart contract on the Ethereum network which will act as a decentralized, anonymous, uncensored, peer-reviewed journal.</p>
        <p><a href="http://www.github.com/delphicrypto/Pear" target="_blank"><button class="button">Contribute</button></a></p>
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="/archives/Images/proposal.svg" alt="Proposal" id="project">
      <div class="container">
        <h2>Research Article</h2>
        <p class="title">Bitcoin consensus algorithm [Peer Reviewed]</p>
        <p>Proposal to update the proof-of-work scheme to divert some of the computational power involved in hashing to solve NP-complete problems</p>
        <p><a href="http://ledger.pitt.edu/ojs/ledger/article/view/194" target="_blank"><button class="button">Article</button></a></p>
      </div>
    </div>
  </div>

</div>

