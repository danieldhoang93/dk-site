<template>
<div>
    <q-select dark dense outlined v-model="location" :options="locations" label="Location" class="q-pb-lg" style="width: 300px"/>

    <div class="" style="max-width: 300px">
        <q-input dark dense outlined v-model="checkIn" mask="date" :rules="['date']" label="Check In">
        <template v-slot:append>
            <q-icon name="event" class="cursor-pointer">
            <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">
                <q-date v-model="checkIn" @input="() => $refs.qDateProxy.hide()" color="secondary"/>
            </q-popup-proxy>
            </q-icon>
        </template>
        </q-input>
    </div>

    <div class="inline" style="max-width: 300px">
        <q-input dark dense outlined v-model="checkOut" mask="date" :rules="['date']" label="Check Out">
        <template v-slot:append>
            <q-icon name="event" class="cursor-pointer">
            <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">
                <q-date v-model="checkOut" @input="() => $refs.qDateProxy.hide()" color="secondary"/>
            </q-popup-proxy>
            </q-icon>
        </template>
        </q-input>
    </div>

    <div class="row" style="max-width: 300px">
        <q-btn-group style="width: 150px">
        <q-btn dense outline round color="white" icon="remove" @click="minusGuest"/>
        <div class="">
            <q-input
            v-model.number="guests"
            dark
            dense
            square 
            disable 
            outlined
            label="Guests"
            />
        </div>
        <q-btn dense outline round color="white" icon="add" @click="addGuest"/>
        </q-btn-group>
        <q-space/>
        <div>
            <q-btn solid color="secondary" text-color="white" label="Search" style="width: 140px; height:40px;" v-bind:to="listingsLink"/>
        </div>
    </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      checkIn: '',
      checkOut: '',
      location: 'Select a location',
      locations: [
        'Florida', 'New Jersey'
      ],
      guests:0,
      listingsLink:'/listings'
    }
  },
  methods: {
        addGuest: function() {
            this.guests += 1;
        },
        minusGuest: function() {
            if (this.guests != 0) {
              this.guests -= 1;
            }
        }
    }
}
</script>