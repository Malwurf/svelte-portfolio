<script>

</script>

<style lang="scss">
  .contact-card {
    display: flex;
    flex-direction: column;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    transition: box-shadow, var(--transition-time);
    padding: 21px;
    &:hover {
      box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
    }
  }
</style>

<section class="contact-card">
  <div class="selfie">
    <img src="" alt="" />
  </div>
  <div class="name">Przemysław Korościk</div>
  <a href="mailto:przemyslaw.koroscik@gmail.com">
    przemyslaw.koroscik@gmail.com
  </a>
  <span class="phone">show</span>
  <span class="sentence">"It's always worth talking"</span>
  <ul class="socials-list">
    <li class="item">
      <a href="https://twitter.com/Malwurf" target="_blank">TT</a>
    </li>
    <li class="item">
      <a href="https://www.linkedin.com/in/przemek-krecik" target="_blank">
        LI
      </a>
    </li>
    <li class="item">
      <a href="http://m.me/kreciik.krecik" target="_blank">FB</a>
    </li>
  </ul>
  <div class="donate">donate</div>
</section>
