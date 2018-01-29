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
        <p>Smart contract on the Ethereum network which will act as a decentralized, anoymous, uncensored, peer-reviewed journal.</p>
        <p><button class="button">Contribute</button></p>
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img src="/archives/Images/proposal.svg" alt="Proposal" id="project">
      <div class="container">
        <h2>Proposal</h2>
        <p class="title">Bitcoin consensus algorithm update</p>
        <p>Proposal to update the proof-of-work scheme to divert some of the computational power involved in hashing to solve NP-complete problems</p>
        <p><button class="button">Article</button></p>
      </div>
    </div>
  </div>

</div>

<div class="row">
  <div class="column">
    <div class="card">
      <img src="/archives/Images/grape.svg" alt="GRAPE" id="project">
      <div class="container">
        <h2>Grape</h2>
        <p class="title">Decentralized Journal</p>
        <p>Decentralized, anoymous, uncensored, peer-reviewed journal built on a DAG (directed acyclic graph).</p>
        <p><button class="button">Contribute</button></p>
      </div>
    </div>
  </div>

  <!--<div class="column">-->
    <!--<div class="card">-->
      <!--<img src="/archives/Images/proposalmessy.svg" alt="Wiki" id="person">-->
      <!--<div class="container">-->
        <!--<h2>Wiki</h2>-->
        <!--<p class="title">Informational Database</p>-->
        <!--<p>Wiki containing information about basic concepts associated with blockchain technology as well as information about the different blockchain projects being developed</p>-->
        <!--<p><button class="button">Link</button></p>-->
      <!--</div>-->
    <!--</div>-->
  <!--</div>-->


  <div class="column">
    <div class="card">
      <img src="/archives/Images/mango.svg" alt="Mango" id="project">
      <div class="container">
        <h2>Mango</h2>
        <p class="title">Investment Tracking Application</p>
        <p>Application keeping track of cryptocurrency investments and working in conjuction with Wiki (coming soon) to categorize investments.</p>
        <p><button class="button">Link</button></p>
      </div>
    </div>
  </div>

</div>
