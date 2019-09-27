<template>
    <div>
       <h2>Zajêcia</h2>
       <new-meeting-form @added="addNewMeeting($event)"></new-meeting-form>
       <meetings-list :meetings="meetings"></meetings-list>
    </div>
</template>

<script>
import NewMeetingForm from "./components/NewMeetingForm";
import MeetingsList from "./components/MeetingsList";

export default {
  components: {NewMeetingForm, MeetingsList},
  data() {
      return {
          meetings: []
      };
  },
  methods: {
      addNewMeeting(meeting) {
          this.meetings.push(meeting);
      }
  }
}
</script>