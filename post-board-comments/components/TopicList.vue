<template>
  <div class="container mt-4">
    <div class="row">
      <div class="col-md-8 offset-md-2">
          <div class="list-group">
            <TopicEntry
              v-for="topic in topics"
              :key="topic.id"
              :topic="topic"
              class="list-group-item"
            />
        </div>
      </div>
    </div>
  </div>
</template>
  
  
<script lang="ts">
  import { defineComponent } from 'vue';
  import TopicEntry from '~/components/TopicEntry.vue';
  
  export default defineComponent({
    components: {
      TopicEntry,
    },
    data() {
      return {
        topics: [
        {
          id: 1,
          image: 'https://picsum.photos/200/300',
          header: 'Topic 1',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec augue ex, ornare ac egestas lacinia, maximus vel tellus. Integer eu varius nunc, non ultricies augue. Vestibulum vehicula scelerisque nunc, eget ultrices sem rhoncus at. Nam vel semper quam. Nam nec nisl ac arcu molestie tincidunt a ut metus. Donec mollis, odio ac semper malesuada, nisl diam iaculis lacus, vitae interdum lectus leo ac dolor. Mauris dolor dui, auctor ac aliquam at, sagittis vel mi.',
          creationDate: '2023-01-10',
          comments: [
            {
              id: 11,
              text: 'Donec pellentesque diam nec porttitor sodales. Nunc ac elit purus. Mauris libero dolor, tempor vitae dui quis, pharetra euismod nulla. Nulla ultrices finibus iaculis. Donec sit amet varius nisl, in laoreet nulla. Ut id neque eu felis consequat pellentesque sit amet ac ligula. Phasellus non placerat est, sit amet tempus diam. Sed non aliquet tellus. In eros tortor, molestie id tincidunt non, sagittis ac velit. In pellentesque justo consectetur sagittis elementum. Nam tempor leo posuere libero tincidunt, eu maximus sem porttitor. Nam pretium tempor magna, a hendrerit sapien. Praesent leo sem, efficitur id bibendum vitae, vehicula id nisi. Nullam eu ultrices sapien. Duis malesuada non leo ut luctus. Vivamus lacinia felis vitae nisi elementum tristique.',
              date: '2023-01-11',
              subComments: [
                {
                  id: 111,
                  text: 'Subcomment Sed facilisis egestas lectus, eu rutrum dolor elementum pharetra. Sed et aliquet augue, nec suscipit quam. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed egestas nulla aliquet, mattis ante eu, sodales nisl. Vestibulum auctor mauris at ex condimentum, ac interdum mi porttitor. Sed tincidunt lectus nisl, id convallis velit ultricies non. Maecenas id viverra ipsum, ut cursus augue. Donec imperdiet consectetur libero et tristique. Duis sit amet sagittis ipsum, quis vehicula diam. Aenean condimentum iaculis nisl sed luctus. Sed ut ante ac neque scelerisque efficitur. Vivamus tincidunt eu nulla at ullamcorper. Etiam semper in enim porta vulputate. Praesent turpis nisi, pretium quis dignissim ut, suscipit et elit. Sed in ipsum sollicitudin, congue nisi quis, blandit elit.',
                  date: '2023-01-17',
                },
              ],
            },
          ],
        },
        {
          id: 2,
          image: 'https://picsum.photos/200',
          header: 'Topic 2',
          description: 'Phasellus mauris urna, pellentesque sed aliquet nec, rhoncus porta lacus. Integer blandit enim non mauris euismod, non finibus nunc ultrices. Mauris pellentesque felis eget sodales molestie. Suspendisse porta sagittis lobortis. Maecenas bibendum, ex nec scelerisque lobortis, sapien sapien porta sapien, eu vehicula ipsum velit at tellus. Curabitur in nibh metus. Sed eget cursus mi. Suspendisse potenti. In ultrices elit a lacus dignissim ornare. Aenean nec pharetra quam. Vivamus sit amet posuere tortor. Etiam ultricies diam at tellus ultrices porttitor.',
          creationDate: '2024-01-12',
          comments: [
            {
              id: 21,
              text: 'In dictum magna enim, vitae vulputate ante rhoncus nec. Cras nulla lorem, iaculis vel hendrerit a, pulvinar vitae velit. Nunc id sem consectetur, luctus tellus vestibulum, consectetur risus. Maecenas consequat arcu diam, ac pharetra tellus venenatis sed. Mauris eget dictum tellus, nec hendrerit ex. Sed rhoncus mauris nibh, eget cursus odio elementum ut. Nullam viverra faucibus lectus. Proin vestibulum dolor felis, at posuere ipsum tempor ut. Quisque finibus ornare condimentum. Duis nec turpis vel urna ullamcorper porta. Donec efficitur sollicitudin augue sed pellentesque. In ultrices volutpat luctus. Praesent vel viverra risus, eget venenatis nulla. Pellentesque id mollis ipsum. Cras feugiat nisl non finibus pulvinar. Pellentesque non tincidunt orci, volutpat posuere quam.',
              date: '2024-01-17',
              subComments: [
                {
                  id: 211,
                  text: 'Morbi pulvinar leo et augue porta, non faucibus arcu tincidunt. Maecenas eros dui, finibus quis facilisis at, tristique id ante. Nulla vehicula consectetur metus vel auctor. Nunc viverra mi tortor, vel congue lorem elementum eget. Integer commodo libero in arcu auctor pretium. Sed rutrum ex ac luctus pretium. Pellentesque a molestie nisi, vitae tincidunt urna.',
                  date: '2024-01-18',
                },
                {
                  id: 256,
                  text: 'Morbi bibendum lorem tortor, et commodo velit congue nec. Praesent ut urna ac eros semper hendrerit quis vel magna. Ut finibus lectus mollis, malesuada dolor quis, dignissim mauris. Nam commodo est quis mauris sagittis tincidunt. Nulla fringilla hendrerit venenatis. Quisque nulla quam, rhoncus a libero et, iaculis sollicitudin orci. Nam pulvinar libero ac sagittis venenatis. Proin vel mauris ac quam convallis malesuada. Aliquam neque massa, suscipit ut commodo a, lacinia at diam. Nunc urna lectus, sodales at gravida interdum, sodales vel nisi. Aenean iaculis a eros non sodales. Vivamus sed urna eget mi dictum pharetra eu ut neque. Ut non libero eget libero bibendum pellentesque.',
                  date: '2022-01-18',
                },
              ],
            },
          ],
        },
        ],
      };
    },
  });
</script>
  