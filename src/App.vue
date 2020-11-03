<template>
  <div id="app">
    <div class="creator">
      <h1 class="brand">
        <!-- <img src="./assets/favicon.png"> -->
        Resume Maker
      </h1>
      <div class="info_header">
        <h4>Personal Informaion</h4>
        <button @click="expandation.expandInfo = !expandation.expandInfo"><i class="fas" :class="{'fa-plus':!expandation.expandInfo,'fa-minus':expandation.expandInfo}"></i></button>
      </div>
      <template v-if="expandation.expandInfo">
        <ul class="creator_list">
          <li class="creator_item">
            <label>Name</label>
            <input type="text" v-model="personalInfo.name" @keypress="beforeInput.firstName = false">
          </li>
          <li class="creator_item">
            <label>Job Title</label>
            <input type="text" v-model="personalInfo.jobTittle" @keypress="beforeInput.firstPosition = false">
          </li>
          <li class="creator_item">
            <label>Age</label>
            <div class="dob_container">
              <select name="DOBDay" v-model="personalInfo.dob.day">
                <option disabled>Day</option>
                <option value="1">1</option>
                <option value="2">2</option>
                <option value="3">3</option>
                <option value="4">4</option>
                <option value="5">5</option>
                <option value="6">6</option>
                <option value="7">7</option>
                <option value="8">8</option>
                <option value="9">9</option>
                <option value="10">10</option>
                <option value="11">11</option>
                <option value="12">12</option>
                <option value="13">13</option>
                <option value="14">14</option>
                <option value="15">15</option>
                <option value="16">16</option>
                <option value="17">17</option>
                <option value="18">18</option>
                <option value="19">19</option>
                <option value="20">20</option>
                <option value="21">21</option>
                <option value="22">22</option>
                <option value="23">23</option>
                <option value="24">24</option>
                <option value="25">25</option>
                <option value="26">26</option>
                <option value="27">27</option>
                <option value="28">28</option>
                <option value="29">29</option>
                <option value="30">30</option>
                <option value="31">31</option>
              </select>
              <select name="DOBMonth" v-model="personalInfo.dob.month">
                <option disabled>Month</option>
                <option value="January">January</option>
                <option value="Febuary">Febuary</option>
                <option value="March">March</option>
                <option value="April">April</option>
                <option value="May">May</option>
                <option value="June">June</option>
                <option value="July">July</option>
                <option value="August">August</option>
                <option value="September">September</option>
                <option value="October">October</option>
                <option value="November">November</option>
                <option value="December">December</option>
              </select>
              <select name="DOBYear" v-model="personalInfo.dob.year">
                <option disabled>Year</option>
                <option value="2004">2004</option>
                <option value="2003">2003</option>
                <option value="2002">2002</option>
                <option value="2001">2001</option>
                <option value="2000">2000</option>
                <option value="1999">1999</option>
                <option value="1998">1998</option>
                <option value="1997">1997</option>
                <option value="1996">1996</option>
                <option value="1995">1995</option>
                <option value="1994">1994</option>
                <option value="1993">1993</option>
                <option value="1992">1992</option>
                <option value="1991">1991</option>
                <option value="1990">1990</option>
                <option value="1989">1989</option>
                <option value="1988">1988</option>
                <option value="1987">1987</option>
                <option value="1986">1986</option>
                <option value="1985">1985</option>
                <option value="1984">1984</option>
                <option value="1983">1983</option>
                <option value="1982">1982</option>
                <option value="1981">1981</option>
                <option value="1980">1980</option>
                <option value="1979">1979</option>
                <option value="1978">1978</option>
                <option value="1977">1977</option>
                <option value="1976">1976</option>
                <option value="1975">1975</option>
                <option value="1974">1974</option>
                <option value="1973">1973</option>
                <option value="1972">1972</option>
                <option value="1971">1971</option>
                <option value="1970">1970</option>
                <option value="1969">1969</option>
                <option value="1968">1968</option>
                <option value="1967">1967</option>
                <option value="1966">1966</option>
                <option value="1965">1965</option>
                <option value="1964">1964</option>
                <option value="1963">1963</option>
                <option value="1962">1962</option>
                <option value="1961">1961</option>
                <option value="1960">1960</option>
                <option value="1959">1959</option>
                <option value="1958">1958</option>
                <option value="1957">1957</option>
                <option value="1956">1956</option>
                <option value="1955">1955</option>
                <option value="1954">1954</option>
                <option value="1953">1953</option>
                <option value="1952">1952</option>
                <option value="1951">1951</option>
                <option value="1950">1950</option>
                <option value="1949">1949</option>
                <option value="1948">1948</option>
                <option value="1947">1947</option>
                <option value="1946">1946</option>
                <option value="1945">1945</option>
                <option value="1944">1944</option>
                <option value="1943">1943</option>
                <option value="1942">1942</option>
                <option value="1941">1941</option>
                <option value="1940">1940</option>
                <option value="1939">1939</option>
                <option value="1938">1938</option>
                <option value="1937">1937</option>
                <option value="1936">1936</option>
                <option value="1935">1935</option>
                <option value="1934">1934</option>
                <option value="1933">1933</option>
                <option value="1932">1932</option>
                <option value="1931">1931</option>
                <option value="1930">1930</option>
              </select>
            </div>
          </li>
          <li class="creator_item">
            <label>E-mail</label>
            <input type="email" v-model="personalInfo.mail">
          </li>
          <li class="creator_item">
            <label>Phone</label>
            <input type="number" v-model="personalInfo.phone">
          </li>
          <li class="creator_item">
            <label>Gender</label>
            <div class="radio_container"><input type="radio" name="gender" @change="personalInfo.male = true"><label>Male</label></div>
            <div class="radio_container"><input type="radio" name="gender" @change="personalInfo.male = false"><label>Female</label></div>
          </li>
          <li class="creator_item" v-if="personalInfo.male">
            <label>Military Service Status</label>
            <select v-model="personalInfo.milStatus">
              <option value="postponed">Postponed</option>
              <option value="exemption">Exemption</option>
              <option value="fulfilled">Fulfilled</option>
            </select>
          </li>
          <li class="creator_item">
            <label>Marital Status</label>
            <select v-model="personalInfo.marStatus">
              <option value="single">Single</option>
              <option value="married">Married</option>
              <option value="divorced">Divorced</option>
              <option value="widowed">Widowed</option>
            </select>
          </li>
        </ul>
        <div class="creator_item" id="links">
          <div class="custom_container"><label>Links</label><button class="custom_btn" @click="beforeInput.customLink = !beforeInput.customLink">{{!beforeInput.customLink?'Custom Link':'Existed Link'}}</button></div>
          <template v-if="!beforeInput.customLink" >
            <select ref="link">
              <option value="siteName" disabled selected>SiteName</option>
              <option value="facebook">Facebook</option>
              <option value="twitter">Twitter</option>
              <option value="linkedin">Linkedin</option>
              <option value="gitHub">GitHub</option>
              <option value="codepen">CodePen</option>
              <option value="behance">Behance</option>
            </select>
            <input type="text" placeholder="Paste link" ref="siteLink">
            <button class="btn_main2" @click="addLinkTarget()">Add</button>
          </template>
          <template id="custom_links" v-if="beforeInput.customLink">
            <input type="text" placeholder="Site Name" ref="customSite">
            <input type="text" placeholder="Paste link" ref="customSiteLink">
            <input type="color" ref="customLinkColor">
            <button class="btn_main2" @click="addLinkCustom()">Add</button>
          </template>
        </div>
      </template>
      <div class="edu_header">
        <h4>Education</h4>
        <button @click="expandation.expandEdu = !expandation.expandEdu"><i class="fas" :class="{'fa-plus':!expandation.expandEdu,'fa-minus':expandation.expandEdu}"></i></button>
      </div>
      <template v-if="expandation.expandEdu">
        <ul class="creator_list">
          <li class="creator_item">
            <label>Degree</label>
            <input type="text" v-model="eductionalInfo.degree" @keypress="beforeInput.firstDegree = false">
          </li>
          <li class="creator_item">
            <label>University</label>
            <input type="text" v-model="eductionalInfo.university" @keypress="beforeInput.firstUniversity = false">
          </li>
          <li class="creator_item">
            <label>Faculty</label>
            <input type="text" v-model="eductionalInfo.faculty" @keypress="beforeInput.firstFaculty = false">
          </li>
        </ul>
      </template>
      <div class="lang_header">
        <h4>Languages</h4>
        <button @click="expandation.expandLang = !expandation.expandLang"><i class="fas" :class="{'fa-plus':!expandation.expandLang,'fa-minus':expandation.expandLang}"></i></button>
      </div>
      <template v-if="expandation.expandLang">
        <div class="lang_container">
          <ul v-for="(lang, index) in languages" :key="lang">
            <li>
              {{ lang.name }}  <button><i class="fas fa-times" id="index" @click="languages.splice(index,1)"></i></button>
            </li>
          </ul>
        </div>
        <ul class="creator_list">
          <li class="creator_item">
            <label>Language</label>
            <input type="text" ref="lang">
          </li>
          <li class="creator_item">
            <label>Level</label>
            <input type="text" ref="level">
          </li>
          <button class="btn_main" @click="addLang()">Add</button>
        </ul>
      </template>
      <div class="skills_header">
        <h4>Skills</h4>
        <button @click="expandation.expandSkills = !expandation.expandSkills"><i class="fas" :class="{'fa-plus':!expandation.expandSkills,'fa-minus':expandation.expandSkills}"></i></button>
      </div>
      <template v-if="expandation.expandSkills">
        <div class="skills_container">
          <ul v-for="(skill, index) in skills" :key="skill">
            <li>
              {{ skill }}  <button><i class="fas fa-times" @click="skills.splice(index,1)"></i></button>
            </li>
          </ul>
        </div>
        <ul class="creator_list">
          <li class="creator_item">
            <label>Skill</label>
            <input type="text" ref="skill">
          </li>
          <button class="btn_main" @click="addSkills()">Add</button>
        </ul>
      </template>
      <div class="proj_header">
        <h4>Projects</h4>
        <button @click="expandation.expandProj = !expandation.expandProj"><i class="fas" :class="{'fa-plus':!expandation.expandProj,'fa-minus':expandation.expandProj}"></i></button>
      </div>
      <template v-if="expandation.expandProj">
        <div class="projects_container">
          <ul v-for="(proj, index) in projects" :key="proj.name">
            <li>
              {{ proj.name }}  <button><i class="fas fa-times" @click="projects.splice(index,1)"></i></button>
            </li>
          </ul>
        </div>
        <ul class="creator_list">
          <li class="creator_item">
            <label>Name</label>
            <input type="text" ref="projName">
          </li>
          <li class="creator_item">
            <label>Company</label>
            <input type="text" ref="company">
          </li>
          <li class="creator_item">
            <label>Responsibilities</label>
            <textarea rows="10" placeholder="Type responsibilities or learned values if the project was self learning..." ref="description"></textarea>
          </li>
          <button class="btn_main" @click="addProjects()">Add</button>
        </ul>
      </template>
      <button class="btn_main" @click="download()">Download HTML</button>
      <button class="btn_main" @click="generatePDF()">Download PDF</button>
    </div>
    <div class="resume_template">
      <div class="container">
          <div class="header">
              <h1 class="name">
                  {{ personalInfo.name }}
              </h1>
              <h1 class="name" v-if="beforeInput.firstName">
                  Name
              </h1>
              <p class="position">
                  {{ personalInfo.jobTittle }}
              </p>
              <p class="position" v-if="beforeInput.firstPosition">
                  Job Tittle
              </p>
              <div class="info_container">
                  <ul class="info_list">
                      <li class="info_item">
                          <span>Address:</span> {{ personalInfo.address }}
                      </li>
                      <li class="info_item">
                          <span>Military Service Status:</span> {{ personalInfo.milStatus }}
                      </li>
                      <li class="info_item">
                          <span>Marital Status:</span> {{ personalInfo.marStatus }}
                      </li>
                  </ul>
                  <ul class="info_list">
                      <li class="info_item">
                          <span>Date of birth:</span> {{ personalInfo.dob.day }}/{{ personalInfo.dob.month }}/{{ personalInfo.dob.year }}
                      </li>
                      <li class="info_item">
                          <span>Phone:</span> {{ personalInfo.phone }}
                      </li>
                      <li class="info_item">
                          <span>E-mail:</span> <input type="text" id="mail" v-model="personalInfo.mail" readonly> <button v-if="personalInfo.mail" onclick="copyMail()" class="btn">copy</button>
                      </li>
                  </ul>
              </div>
              <p class="info_item">
                  <span>Find me online:</span> <span v-for="(link, index) in linksArr" :key="index" v-html="link"></span>
              </p>
          </div>
          <div class="flex">
              <div class="edu">
                  <h1>Education</h1>
                  <h3 class="degree">{{ eductionalInfo.degree }}</h3>
                  <h3 class="degree" v-if="beforeInput.firstDegree">Degree</h3>
                  <p class="university">{{ eductionalInfo.university }}</p>
                  <p class="university" v-if="beforeInput.firstUniversity">University</p>
                  <p class="faculty">{{ eductionalInfo.faculty }}</p>
                  <p class="faculty" v-if="beforeInput.firstFaculty">Faculty</p>
              </div>
              <div class="lang">
                  <h1>Languages</h1>
                  <template v-for="lang in languages">
                    <div :key="lang.name">
                      <h3>{{lang.name}}</h3>  <p>{{ lang.level }}</p>
                    </div>
                  </template>
                  <div v-if="beforeInput.firstLanguage">
                      <h3>Language 1</h3>  <p>Native</p>
                  </div>
                  <div v-if="beforeInput.firstLanguage">
                      <h3>Language 2</h3>  <p>Good</p>
                  </div>
              </div>
              <div class="skilles">
                  <h1>Skills</h1>
                  <div class="skills_list">
                      <ul v-for="skill in skills" :key="skill">
                          <li class="skill">
                              {{ skill }}
                          </li>
                      </ul>
                      <ul v-if="beforeInput.firstSkill">
                          <li class="skill">
                              Skill 1
                          </li>
                          <li class="skill">
                              Skill 2
                          </li>
                          <li class="skill">
                              Skill 3
                          </li>
                          <li class="skill">
                              Skill 4
                          </li>
                          <li class="skill">
                              Skill 5
                          </li>
                      </ul>
                  </div>
              </div>
          </div>
          <div class="proj">
              <h1>Projects</h1>
              <div class="proj_container">
                <template v-for="project in projects">
                  <div class="proj_job" :key="project.name">
                      <h3 class="proj_tittle">{{ project.name }}</h3>
                      <p class="proj_type">{{ project.company }}</p>
                      <p class="desc">
                        {{ project.desc }}
                      </p>
                  </div>
                </template>
                <div class="proj_job" v-if="beforeInput.firstProject">
                    <h3 class="proj_tittle">Project Name</h3>
                    <p class="proj_type">Company Name</p>
                    <ul class="desc">
                        <li class="resp">
                            Responsibilities and deescription
                        </li>
                    </ul>
                </div>
                <div class="proj_job" v-if="beforeInput.firstProject">
                    <h3 class="proj_tittle">Project Name 2</h3>
                    <p class="proj_type">Company Name</p>
                    <ul class="desc">
                        <li class="resp">
                            Responsibilities and deescription
                        </li>
                    </ul>
                </div>
              </div>
          </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'app',
  data () {
    return {
      personalInfo:{
        name:'',
        jobTittle: '',
        address: '',
        dob: {
          day:'Day',
          month:'Month',
          year:'Year'
        },
        phone:null,
        mail:'',
        male: null,
        milStatus:'',
        marStatus:''
      },
      eductionalInfo: {
        degree:'',
        university:'',
        faculty:''
      },
      languages: [],
      skills: [],
      projects: [],
      links: ['facebook', 'twitter', 'gitHub', 'codepen', 'linkedin', 'behance'],
      linksArr:[],
      beforeInput: {
        firstProject: true,
        firstSkill: true,
        firstLanguage: true,
        firstDegree: true,
        firstUniversity: true,
        firstFaculty: true,
        firstName: true,
        firstPosition: true,
        customLink: false
      },
      expandation: {
        expandInfo: false,
        expandEdu: false,
        expandLang: false,
        expandSkills: false,
        expandProj: false
      },
      resumeStyle: `body{
      @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap');
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Roboto', sans-serif;
        font-size: 15px;
        background: #ffffff;
        color: #000;
      }
      .container{
          margin: 1em;
          min-height: 90vh;
      }
      .container div{
          margin-top: 1em;
      }
      .header{
          background: #f1f1f1;
          width: 100%;
          border-radius: 5px;
          padding: 1em;
          text-align: center;
      }
      .info_container{
          display: flex;
          
      }
      ul,
      li{
          list-style: none;
          margin: auto;
      }
      .info_list{
          text-align: left;
      }
      .info_item{
          margin-top: 1em;
          margin-left: 4em;
          text-transform: capitalize;
      }
      .btn{
          display: inline-block;
          padding: 0.2em 0.5em;
          margin-left: 0.5em;
          border-radius: 5px;
          background: #1d1d1d;
          color: #ffffff;
          text-decoration: none;
          font-weight: 700;
          border: none;
          outline: none;
          cursor: pointer;
      }
      .linkedin{
          background: #006097;
      }
      .gitHub{
          background: #24292e;
      }
      .twitter{
          background: #3598e9;
      }
      .codepen{
          background: #444857;
      }
      .facebook{
          background: #385898;
      }
      .behance{
      background: #3379ff;
      }
      .info_item span:first-child{
          font-weight: 700;
      }
      #mail{
          border: none;
          background: transparent;
          outline: none;
          font-size: 1rem;
          min-width: 12em;
          margin-right: 1em;
      }
      .skills_list{
          display: flex;
          justify-content: space-between;
          align-items: center;
          text-align: left;
      }
      .flex{
          display: flex;
          justify-content: center;
          align-items: center;
      }
      .skilles h1,
      .edu h1,
      .lang h1{
          margin-bottom: 1em;
          text-align: center;
      }
      .skilles,
      .edu,
      .lang{
          width: 300%;
          text-align: left;
          margin: 1em 4em;
          padding: 0 2em;
      }
      .lang{
          text-align: center;
      }
      .lang div{
          display: inline-block;
          padding: 0 1em;
      }
      .proj{
          text-align: center;
      }
      .proj_container{
          display: grid;
          grid-template-columns: repeat(2, 1fr);
          
      }
      .proj_job{
          background: #f1f1f1;
          margin-right: 1em;
          padding: 1em;
          border-radius: 3px;
          text-align: left;
      }
      .proj_tittle{
          text-align: center;
      }
      .proj_type{
          color: #5a5a5a;
          text-indent: 1em;
      }
      .desc{
        white-space: pre-line;
      }`
    }
  },
  methods: {
    copyMail: ()=>{
      const mail = document.getElementById('mail')
      mail.select();
      mail.setSelectionRange(0, 30);
      document.execCommand("copy");
      alert("E-mail Copied: " + mail.value);
    },
    addLang: function(){
      const lang = this.$refs.lang.value,
            level = this.$refs.level.value,
            langObj = {name:lang, level:level}
      this.languages.push(langObj)
      this.$refs.lang.value = ''
      this.$refs.level.value = ''
      this.firstLanguage = false
    },
    addSkills: function(){
      const skill = this.$refs.skill.value
      this.skills.push(skill)
      this.$refs.skill.value = ''
      this.firstSkill = false
    },
    addProjects: function(){
      const name = this.$refs.projName.value,
            company = this.$refs.company.value,
            desc = this.$refs.description.value,
            projObj = {name: name, company: company, desc: desc}
      this.projects.push(projObj)
      this.$refs.projName.value = ''
      this.$refs.company.value = ''
      this.$refs.description.value = ''
      this.firstProject = false
    },
    addLinkTarget: function(){
      let siteName = this.$refs.link.value
      let string = this.links.includes(siteName)?`<a href="${this.$refs.siteLink.value}" target="_blank" class="btn ${siteName}">${siteName}</a>`:''
        this.linksArr.push(string)
      this.$refs.link.value = 'siteName'
      this.$refs.siteLink.value = ''
    },
    addLinkCustom: function(){
      let siteName, siteLink, siteColor, string
      siteName = this.$refs.customSite.value
      siteLink = this.$refs.customSiteLink.value
      siteColor = this.$refs.customLinkColor.value
      if(siteName && siteName !== ' ' && siteLink && siteLink !== ' '){
        string =`<a href="${siteLink}" target="_blank" class="btn" style="background: ${siteColor};">${siteName}</a>`
        this.linksArr.push(string)
      }
      this.$refs.customSite.value = ''
      this.$refs.customSiteLink.value = ''
    },
    download: function(data = `
<!DOCTYPE html>
<html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>${this.personalInfo.name} Resume</title>
  </head>
  <body>
    <style>${this.resumeStyle}</style>
    ${document.querySelector('.resume_template').innerHTML}
    </body>
</html>`, filename = 'Resume', type = 'text/html') {
    var file = new Blob([data], {type: type});
    if (window.navigator.msSaveOrOpenBlob) // IE10+
        window.navigator.msSaveOrOpenBlob(file, filename);
    else { // Others
        var a = document.createElement("a"),
                url = URL.createObjectURL(file);
        a.href = url;
        a.download = filename;
        document.body.appendChild(a);
        a.click();
        setTimeout(function() {
            document.body.removeChild(a);
            window.URL.revokeObjectURL(url);  
        }, 0); 
      }
    },
    generatePDF: function() {
        const element = document.querySelector('.resume_template');
        html2pdf()
          .from(element)
          .save();
      }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700;900&display=swap');
:root{
  --main: #42b983;
  --bgcolor: #202020;
  --secondbg: #333333;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  background: var(--secondbg);
  height: 100%;
}
#app {
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: grid;
  grid-template-columns: 1fr 4fr;
  color: #f1f1f1;
}
input[type=number] { 
  -moz-appearance: textfield;
  appearance: textfield;
  margin: 0; 
}
input[type=number]::-webkit-inner-spin-button, 
input[type=number]::-webkit-outer-spin-button { 
  -webkit-appearance: none; 
  margin: 0; 
}
.creator{
  background: var(--bgcolor);
  min-height: 100vh;
  border-right: var(--main) 2px solid;
  .btn_main{
    width: fit-content;
    margin-left: 0.2em;
    margin-bottom: 1em;
  } 
}
.creator_list{
  list-style: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
}
.brand{
  color: var(--main);
  font-weight: 900;
  font-size: 2rem;
  padding: 0.5em;
}

.info_header, .edu_header, .lang_header, .skills_header, .proj_header{
  padding: 1em;
  margin-bottom: 1em;
  display: flex;
  justify-content: space-between;
  color: var(--main);
  background: var(--secondbg);
  button{
    background: transparent;
    border: none;
    outline: none;
    cursor: pointer;
    i{
    font-size: 1rem;
    background: transparent;
    color: var(--main);
    transition: all 1s ease;
  }
  }
  
}
.dob_container{
  display: grid;
  grid-template-columns: 2fr 3fr 2fr;
  select{
    box-shadow: none !important;
  }
}
.creator_item{
  display: grid;
  grid-template-columns: 1fr;
  text-align: left;
  width: 85%;
  margin: 0.5em auto;
  label{
    color: var(--main);
    margin: 0 0.3em;
  }
  input, select, button, textarea{
    outline: none;
    background: var(--secondbg);
    border: none;
    font-size: 1rem;
    color: var(--main);
    padding: 0.5em;
    width: 100%;
    box-shadow: 0 5px 25px rgba(0, 0, 0, 0.2);
    font-family: 'Roboto', sans-serif;
    resize: none;
    option{
      border: none;
      outline: none;
    }
  }
  button ,select{
    cursor: pointer;
  }
}
.radio_container:nth-of-type(1){
  margin-top: 1em;
}
.radio_container{
  display: flex;
  align-content: center;
  input{
    margin-left: 0.5em;
    width: 5%;
    padding: 0;
    margin: 0.1em;
  }
}
#links{
  .custom_container{
    display: flex;
    align-content: center;
    justify-content: center;
  }
  .custom_btn{
  margin-right: 0;
  width: fit-content;
  margin-bottom: 1em;
  margin-top: 0;
  border-radius: 1em;
  }
  input[type="color"] {
	-webkit-appearance: none;
	border: none;
  height: 40px;
  background: transparent;
}
input[type="color"]::-webkit-color-swatch-wrapper {
	padding: 0;
}
input[type="color"]::-webkit-color-swatch {
	border: none;
}
  select{
    width: 60%;
    padding: 0.5em;
    margin: auto;
    box-shadow: 0 5px 25px rgba(0, 0, 0, 0.2);
    border-bottom: solid 1px var(--main);
  option{
    min-height: 3em !important;
  }
  }
  button{
    margin: auto;
    margin-top: 0.5em;
    width: 30%;
  }
  input{
    margin-top: 1em;
    outline: none;
    background: var(--secondbg);
    border: none;
    font-size: 1rem;
    color: var(--main);
    padding: 0.5em;
    width: 100%;
    box-shadow: 0 5px 25px rgba(0, 0, 0, 0.2);
  }
}
.skills_container, .lang_container, .projects_container{
  ul{
    list-style: none;
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin: 0.5em 1em;
    flex-basis: 50%;
    flex-wrap: wrap;
    li{
      margin: 0.3em auto;
      margin-left: 0.5em;
      background: var(--secondbg);
      padding: 0.5em;
      border-radius: 1em;
      color: var(--main);
      width: fit-content;
      display: flex;
      justify-content: space-between;
      align-items: center;
      button{
        background: transparent;
        border: none;
        outline: none;
        margin-left: 0.3em;
        cursor: pointer;
        i{
          font-size: 1rem;
          background: transparent;
          color: var(--main);
          transition: all 1s ease;
        }
      }
    } 
  }
}
.btn_main{
  outline: none;
  background: var(--secondbg);
  border: none;
  margin: auto;
  margin-bottom: 1em;
  font-size: 1rem;
  color: var(--main);
  padding: 0.5em 1em;
  box-shadow: 0 5px 25px rgba(0, 0, 0, 0.2);
  cursor: pointer;
}
      

    // resume Style

.resume_template{
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap');
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
    font-size: 15px;
    background: #ffffff;
    color: #000;
}
.container{
    margin: 1em;
    min-height: 90vh;
}
.container div{
    margin-top: 1em;
}
.header{
    background: #f1f1f1;
    width: 100%;
    border-radius: 5px;
    padding: 1em;
    text-align: center;
}
.info_container{
    display: flex;
    
}
ul,
li{
    list-style: none;
    margin: auto;
}
.info_list{
    text-align: left;
}
.info_item{
    margin-top: 1em;
    margin-left: 4em;
    text-transform: capitalize;
}
.btn{
    display: inline-block;
    padding: 0.2em 0.5em;
    margin-left: 0.5em;
    border-radius: 5px;
    background: #1d1d1d;
    color: #ffffff;
    text-decoration: none;
    font-weight: 700;
    border: none;
    outline: none;
    cursor: pointer;
}
.linkedin{
    background: #006097;
}
.gitHub{
    background: #24292e;
}
.twitter{
    background: #3598e9;
}
.codepen{
    background: #444857;
}
.facebook{
    background: #385898;
}
.behance{
background: #3379ff;
}
.info_item span:first-child{
    font-weight: 700;
}
#mail{
    border: none;
    background: transparent;
    outline: none;
    font-size: 1rem;
    min-width: 12em;
    margin-right: 1em;
}
.skills_list{
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: left;
}
.flex{
    display: flex;
    justify-content: center;
    align-items: center;
}
.skilles h1,
.edu h1,
.lang h1{
    margin-bottom: 1em;
    text-align: center;
}
.skilles,
.edu,
.lang{
    width: 300%;
    text-align: left;
    margin: 1em 4em;
    padding: 0 2em;
}
.lang{
    text-align: center;
}
.lang div{
    display: inline-block;
    padding: 0 1em;
}
.proj{
    text-align: center;
}
.proj_container{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    
}
.proj_job{
    background: #f1f1f1;
    margin-right: 1em;
    padding: 1em;
    border-radius: 3px;
    text-align: left;
}
.proj_tittle{
    text-align: center;
}
.proj_type{
    color: #5a5a5a;
    text-indent: 1em;
}
.desc{
  white-space: pre-line;
}
</style>
