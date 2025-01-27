<link rel="stylesheet" href="/assets/style/welcome.css" as="style" />
<div class="top2Sections">
  <section class="welcomeWords">
    <div class="main">
      <div>
        <h2 class="welcomeTitle">Добро пожаловать в SubQuery’s <span>Docs</span></h2>
        <p>Исследуйте и преобразуйте данные цепочки, чтобы быстрее создавать интуитивно понятные приложения!</p>
      </div>
    </div>
  </section>
  <section class="startSection main">
    <div>
      <h2 class="title">Быстрый старт <span>Гид</span></h2>
      <p>Понимайте SubQuery, используя традиционный пример Hello World. Использование шаблона проекта с помощью Докера , вы можете быстро запустить узел и начать искать данные в блокчейне всего за несколько минут с помощью нескольких простых команд.
      </p>
      <span class="button">
        <router-link :to="{path: '/quickstart/helloworld-localhost/'}">
          <span>Начать</span>
        </router-link>
      </span>
    </div>
  </section>
</div>
<div class="main">
  <div>
    <ul class="list">
      <li>
        <router-link :to="{path: '/tutorials_examples/introduction/'}">
          <div>
            <img src="/assets/img/tutorialsIcon.svg" />
            <span>Учебные материалы и примеры</span>
            <p>Обучение на практике Обучение на практике Учебники и примеры по созданию различных проектов SubQuery.</p>
          </div>
        </router-link>
      </li>
      <li>
        <router-link :to="{path: '/create/introduction/'}">
          <div>
            <img src="/assets/img/docsIcon.svg" />
            <span>Техническая документация</span>
            <p>Написано разработчиками для разработчиков. Найдите то, что нужно для быстрого создания приложений.</p>
          </div>
        </router-link>
      </li>
      <li>
        <a href="https://static.subquery.network/whitepaper.pdf" target="_blank">
          <div>
            <img src="/assets/img/networkIcon.svg" />
            <span>The SubQuery Network</span>
            <p>Децентрализованное будущее SubQuery. Подробнее о вознаграждении индексаторов и потребителей.</p>
          </div>
        </a>
      </li>
    </ul>
  </div>
</div>
<section class="faqSection main">
  <div>
    <h2 class="title">Часто задаваемые вопросы</h2>
    <ul class="faqList">
      <li>
        <div class="title">Что такое SubQuery?</div>
        <div class="content">
          <p>SubQuery - это проект с открытым исходным кодом, который позволяет разработчикам индексировать, преобразовывать и запрашивать данные цепочки Substrate для работы своих приложений.</p>
          <span class="more">
            <router-link :to="{path: '/faqs/faqs/#what-is-subquery'}">ЧИТАТЬ БОЛЬШЕ</router-link>
          </span>
        </div>
      </li>
      <li>
        <div class="title">Как лучше всего начать работу с SubQuery?</div>
        <div class="content">
          <p>Лучший способ начать работу с SubQuery - попробовать наш туториал <a href="/quickstart/helloworld-localhost/"> Привет, Мир </a>. Это простой 5-минутный урок по загрузке стартового шаблона, сборке проекта, а затем использованию Docker для запуска узла на локальном хосте и выполнения простого запроса. </p>
        </div>
      </li>
      <li>
        <div class="title">Как я могу внести свой вклад или оставить отзыв о SubQuery?</div>
        <div class="content">
          <p>Нам нравится вклад и обратная связь с сообществом. Чтобы внести свой код, форкните интересующий вас репозиторий и внесите свои изменения. Далее отправьте PR или Pull Request. О, не забудьте также протестировать! Также ознакомьтесь с нашими рекомендациями по взносам (скоро появятся). </p>
          <span class="more">
            <router-link :to="{path: '/faqs/faqs/#what-is-the-best-way-to-get-started-with-subquery'}">Узнайте больше</router-link>
          </span>
        </div>
      </li>
      <li>
        <div class="title">Сколько стоит размещение моего проекта в SubQuery?</div>
        <div class="content">
          <p>Размещение вашего проекта в SubQuery абсолютно бесплатно - это наш способ отблагодарить сообщество. Чтобы узнать, как разместить свой проект у нас, ознакомьтесь с руководством <a href="/quickstart/helloworld-hosted/"> Привет, Мир (SubQuery Hosted)</a>.</p>
          <span class="more">
            <router-link :to="{path: '/publish/publish/'}"> РАЗМЕЩЕНИЕ ВАШЕГО ПРОЕКТА</router-link>
          </span>
        </div>
      </li>
    </ul><br>
    Для получения дополнительной информации по часто задаваемым вопросам, пожалуйста, ознакомьтесь с нашей <router-link :to="{path: '/faqs/faqs/'}">Страницей часто задаваемых вопросов (FAQ)</router-link> странице.    
  </div>
</section>
<section class="main">
  <div>
    <div class="lastIntroduce lastIntroduce_1">
        <h5>Интеграция с вашей пользовательской цепочкой?</h5>
        <p>Создаете ли вы новый парачейн или совершенно новый блокчейн на Substrate - SubQuery поможет вам индексировать и устранять неполадки в данных вашей цепи. SubQuery разработан для легкой интеграции с пользовательской цепочкой на основе субстрата.</p>
        <span class="more">
          <<router-link :to="{path: '/create/mapping/#custom-substrate-chains'}">УЗНАЙТЕ, КАК ИНТЕГРИРОВАТЬСЯ С ВАШЕЙ ЦЕПОЧКОЙ</router-link>
        </span>
    </div>
    <div class="lastIntroduce lastIntroduce_2">
        <h5>Поддержка и вклад</h5>
        <p>У вас есть вопрос или вы хотите узнать больше или как вы можете внести свой вклад? Мы будем рады услышать вас. Пожалуйста, свяжитесь с нами по электронной почте или в социальных сетях по ссылкам ниже. Нужна техническая поддержка? Присоединяйтесь к нашему сообществу Discord и получайте поддержку от наших неравнодушных членов сообщества. </p>
        <a class="more" target="_blank" href="https://discord.com/invite/78zg8aBSMG">ПРИСОЕДИНЯЙТЕСЬ К ОБСУЖДЕНИЮ В ДИСКОРДЕ</a>
    </div>
    </div>
</section>
<section class="main connectSection">
  <div class="email">
    <span>Свяжитесь с нами</span>
    <a href="mailto:hello@subquery.network">hello@subquery.network</a>
  </div>
  <div>
    <div>Подпишитесь на нас в социальных сетях</div>
    <div class="connectWay">
      <a href="https://discord.com/invite/78zg8aBSMG" target="_blank" class="connectDiscord">discord</a>
      <a href="https://twitter.com/subquerynetwork" target="_blank" class="connectTwitter">twitter</a>
      <a href="https://medium.com/@subquery" target="_blank" class="connectMedium">medium</a>
      <a href="https://t.me/subquerynetwork" target="_blank" class="connectTelegram">telegram</a>
      <a href="https://github.com/OnFinality-io/subql" target="_blank" class="connectGithub">github</a>
      <a href="https://matrix.to/#/#subquery:matrix.org" target="_blank" class="connectMatrix">matrix</a>
      <a href="https://www.linkedin.com/company/subquery" target="_blank" class="connectLinkedin">linkedin</a>
    </div>
  </div>
</section>
</div> </div>
<div class="footer">
  <div class="main"><div>SubQuery © 2021</div></div>
</div>
<script charset="utf-8" src="/assets/js/welcome.js"></script>
