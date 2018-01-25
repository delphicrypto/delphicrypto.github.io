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
      <img src="/archives/Images/pear.png" alt="Pear" id="person" style="width:80%">
      <div class="container">
        <h2>PEAR</h2>
		<p class='title'> PEAR <p>
        <p>Decentralized Journal<p>
        <p>Smart contract on the Ethereum network that acts as a decentralized, anonymous, peer-reviewed journal. </p>
        <p><button class="button">Contribute</button></p>
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="/archives/Images/proposal.png" alt="Mike" style="width:80%" id="person">
      <div class="container">
        <h2>Grape</h2>
		<p class='title'> PEAR <p>
        <p>Decentralized Journal</p>
        <p>Decentralized, anonymous, peer-reviewed journal built on a DAG (directed-acyclic graph)</p>
        <p><button class="button">Contribute</button></p>
      </div>
    </div>
  </div>
</div>

