<template>
<v-container>
  <v-row>
    <v-col>
      <!-- タイトル入力 -->
      {{ title }}
      <v-text-field
        label="Title"
        required
        counter
        maxlength="25"
        @change="(value) => {
          title = value
        }"
      />
      <!-- 詳細入力 -->
      <v-textarea
        label="Description"
        counter
        maxlength="200"
        @change="(value) => {
          description = value
        }"
      />
    </v-col>
    <v-col>
      <v-row>
        <v-col>
          <!-- 時刻選択 -->
          <v-time-picker 
          :value="time"
          format="24hr" 
          @change="(value) => {
            time = value
          }"
          />
        </v-col>
        <v-col>
          <!-- 日付選択 -->
          <v-date-picker
            no-title
            bottom
            color="primary"
          />
        </v-col>
      </v-row>
    </v-col>
    <v-col>
      <!-- 日時選択解除 -->
      <v-list
        class="overflow-y-auto"
        max-height="75vh"
      >
      <date-list-item :date="now"/>
      </v-list>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
  import { DateTime } from 'luxon'

export default{
  data(){
    return{
      now: DateTime.now(),
      title:'',
      description:'',
      time:'19:00',
    }
  }
}
</script>

<style scoped>
</style>