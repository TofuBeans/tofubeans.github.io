<script>
    // User's birthday (YYYY-MM-DD format)
    const birthday = '2010-05-02';

    // User's timezone
    const timezone = 'Europe/London';

    // Function to calculate age based on birthday
    /**
	 * @param {string | number | Date} birthday
	 */
    function calculateAge(birthday) {
        const today = new Date();
        const birthDate = new Date(birthday);
        let age = today.getFullYear() - birthDate.getFullYear();
        const monthDiff = today.getMonth() - birthDate.getMonth();
        if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < birthDate.getDate())) {
            age--;
        }
        return age;
    }

    /**
	 * @param {any} timezone
	 */
    function getCurrentDateTime(timezone) {
        const options = {
            timeZone: timezone,
            weekday: 'long',
            year: 'numeric',
            month: 'long',
            day: 'numeric',
            hour: 'numeric',
        };
        // @ts-ignore
        return new Intl.DateTimeFormat('en-US', options).format(new Date());
    }
</script>

<div class="pronouns-container">
    <a href={"/"} class="special-button" id="backhome">go back to home</a>
    <div class="separator"></div>
    <div class="profile-header">
      <img class="profile-picture" src="pfp.png" alt="Profile Picture"/>
      <h1>Daniella</h1>
    </div>
    <div class="flag" style="margin-bottom: 2em;">
      <img src="trans-flag.png"/>
      <span>Trans</span>
    </div>
    <div class="flag">
      <img src="lesbian-flag.png"/>
      <span>Lesbian</span>
    </div>
    <div class="bio">
      <p>
        <br/>
        <strong>TL;DR;</strong>
        <br/>
        - fem & romantic terms are very good
        <br/>
        - masc very bad
        <br/>
        - idm the rest
      </p>
    </div>
    <div class="age">
      <p><strong>Age: </strong>{"I am currently " + calculateAge(birthday) + " years old."}</p>
    </div>
    <div class="timezone">
      <p><strong>Date & Time: </strong>In my timezone (Europe/London), it is currently <strong>{getCurrentDateTime(timezone)}</strong></p>
    </div>
    <div class="words">
      <div class="separator"></div>
      <div class="group">
        <div class="columns">
          <div class="column">

            <h3 class="group-heading">Names</h3>

            <p><span class="material-icons good" title="preferred">favorite</span>
            <span class="good" title="preferred">Dani</span></p>

            <p><span class="material-icons okay" title="okay">thumb_up</span>
            <span class="okay" title="okay">Daniella</span></p>

            <p><span class="material-icons kys" title="kys">do_not_disturb_on</span>
            <span class="kys" title="kys">[DEADNAME]</span></p>

          </div>
          <div class="column">

            <h3 class="group-heading">Pronouns</h3>

            <p><span class="material-icons good" title="preferred">favorite</span>
            <span class="good" title="preferred">She/Her</span></p>

            <p><span class="material-icons okay" title="okay">thumb_up</span>
            <span class="okay" title="okay">They/Them</span></p>

            <p><span class="material-icons kys" title="kys">do_not_disturb_on</span>
            <span class="kys" title="kys">He/Him</span></p>

          </div>
          <div class="column">

            <h3 class="group-heading">Titles</h3>

            <p><span class="material-icons good" title="preferred">favorite</span>
            <span class="good" title="preferred">Mrs</span></p>

            <p><span class="material-icons kys" title="kys">do_not_disturb_on</span>
            <span class="kys" title="kys">Mr</span></p>

          </div>
        </div>
      </div>
      <div class="separator"></div>
      <div class="group">
        <div class="columns">
          <div class="column">

            <h3 class="group-heading">Compliments</h3>

            <p><span class="material-icons good" title="preferred">favorite</span>
            <span class="good" title="preferred">pretty</span></p>

            <p><span class="material-icons good" title="preferred">favorite</span>
            <span class="good" title="preferred">hot</span></p>

            <p><span class="material-icons okay" title="okay">thumb_up</span>
            <span class="okay" title="okay">cute</span></p>

            <p><span class="material-icons kys" title="kys">do_not_disturb_on</span>
            <span class="kys" title="okay">handsome</span></p>

          </div>
        </div>
      </div>
    </div>
  </div>