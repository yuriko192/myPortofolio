<template>
  <div class="contact_me">
    <div>
      <h5>Address</h5>
      <div>Jl. Vikamas Barat 5 Blok F7 No.6 <br/>
        Kapuk Muara, Penjaringan, Jakarta Utara, 14460
      </div>
    </div>
    <div>
      <h5>Email Me</h5>
      <div>ivanwijaya19@yahoo.co.id</div>
      <div>ivanwijaya19@gmail.com</div>
    </div>
    <div>
      <h5>Message Me</h5>
      <div class="itemslist">
        <div class="item">Telegram</div>
        <div class="item">Line</div>
        <div class="item">Whatsapp</div>
      </div>
    </div>
    <div>
      <h5>My Social Media</h5>
      <div class="itemslist">
        <div class="item">Facebook</div>
        <div class="item">Twitter</div>
        <div class="item">Instagram</div>
      </div>
    </div>
    <div>
      <h5>My Repository</h5>
      <div>github</div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'Contact',
  components: {
  }
}
</script>

<style lang="scss" scoped>
.contact_me{
  padding: 0 10px;
}
.itemslist{
  display: flex;
  justify-content: space-around;
  .item{
    width: 120px;
    text-align: center;
  }
}
</style>