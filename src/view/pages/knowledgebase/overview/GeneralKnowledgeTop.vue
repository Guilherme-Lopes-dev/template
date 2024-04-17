<template>
  <div>
    <KnowledgebaseTopWrap>
      <div class="sDash_knowledgetop">
        <div class="sDash_knowledgetop__search--form">
          <a-form :model="formState" name="login" layout="vertical">
            <div class="sDash_knowledgetop__formInner">
              <a-form-item>
                <a-select v-model:value="formState.type" default-value="Estado">
                  <a-select-option value="email">Email</a-select-option>
                  <a-select-option value="message">Message</a-select-option>
                  <a-select-option value="event">Event</a-select-option>
                </a-select>
              </a-form-item>
              <a-form-item>
                <a-select v-model:value="formState.type" default-value="Cidade">
                  <a-select-option value="email">Email</a-select-option>
                  <a-select-option value="message">Message</a-select-option>
                  <a-select-option value="event">Event</a-select-option>
                </a-select>
              </a-form-item>
              <a-form-item>
                <a-select v-model:value="formState.type" default-value="Especialidade">
                  <a-select-option value="email">Email</a-select-option>
                  <a-select-option value="message">Message</a-select-option>
                  <a-select-option value="event">Event</a-select-option>
                </a-select>
              </a-form-item>
              <a-form-item class="sDash_search-input">
                <a-input v-model:value="formState.search" placeholder="Buscar Especialista..." />
              </a-form-item>
            </div>
          </a-form>
        </div>
      </div>
    </KnowledgebaseTopWrap>
  </div>
</template>

<script>
import { reactive, defineComponent } from 'vue';
import { KnowledgebaseTopWrap } from '../style';
export default defineComponent({
  name: 'GeneralKnowledgeTop',
  components: {
    KnowledgebaseTopWrap,
  },
  setup() {
    const formState = reactive({
      search: '',
      type: undefined,
    });
    return {
      formState,
    };
  },
});
</script>
<style>
.sDash_knowledgetop__formInner{
  border: 1px solid red;
  width: 85%;
  max-width: unset !important;
}

</style>
