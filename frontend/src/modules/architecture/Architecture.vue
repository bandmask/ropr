<template>
  <div class="about">
    <h1 class="header">Architecture</h1>
    <Gallery :images="vm.images"/>
    <div class="content">
      <div>
        <p>
          <s><i class="emphasis">Monoliths</i></s> has for me been the way to develop web. Ever since starting with front end development, using ASP.Net, all the way through MVC .Net and angular. MVC-pattern became the norm and .Net with IIS was the way to host it.
        </p>
        <p>This time we go all in <i class="emphasis">micro.</i></p>
        <p>This time we <i class="emphasis">containerize.</i></p>
      </div>
      <div>
        <h3>Hosting</h3>
        <p>
          Replacing IIS comes with a lot of opportunity and the goal was to go as light weight as possible. Hosting on a single board computer, raspberry, was a good start and from there it grew.
        </p>
        <p>
          The above images are an early mind map for structuring the project, using containerized, self-maintained "pods" with docker.
        </p>
      </div>
      <div>
        <h3>Buzzwords</h3>
        <p>
          <ul>
            <li>Containers</li>
            <li>Docker & Docker Compose</li>
            <li>NodeJs</li>
            <li>Vue</li>
            <li>MongoDb & Redis</li>
          </ul>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Gallery from '@/components/gallery/Gallery'

import imgArchDiscovery from '@/assets/arcitecture_discovery.jpg'
import imgArchContainers from '@/assets/architecture_containers.jpg'

export default {
  components: { Gallery },
  data () {
    return {
      images: [
        {
          src: imgArchDiscovery,
          name: 'Container discovery',
          description: 'Container discovery'
        },
        {
          src: imgArchContainers,
          name: 'Container architecture',
          description: 'Container architecture'
        }
      ]
    }
  },
  computed: {
    vm () {
      return this
    }
  }
}
</script>

<style scoped lang="less">
.about {
  cursor: default;
  user-select: none;

  .content {
    width: 800px;
    margin: 0px auto;
    text-align: left;

    ul {
      margin: 0px;
      padding-left: 20px;
    }

    .emphasis {
      font-weight: 600;
    }
  }
}
</style>
