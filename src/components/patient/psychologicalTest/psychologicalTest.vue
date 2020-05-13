<template>
  <div class="psychologicalTest">
    <el-tabs v-model="activeName" @tab-click="handleClick">
      <!-- <el-tab-pane label="医院简介" name="first">
      <div class="theme">
        <img src="../logo/AnYi.logo.jpg" width="50px" height="50px">
        <span class="span_font">医院简介</span>
      </div>
      <div class="introduction">
      <p style="line-height:30px"><em style="font-size:24px">广州市安逸医院</em>是一家集医疗、教学、科研、预防、保健为一体的非营利性综合二级甲等医院，医院始建于2017年，位于广州市的东面，是广州市著名的公立医院之一，承担市内几十万到几百万人口的医疗、保健、疾病防治任务，是广东省高等医学院教学医院，其影响辐射到整个广州市以及周边地区。
       <p style="line-height:30px;text-indent:2em">医院占地面积4万平方米，建筑面积6万多平方米，现开放病床448张，现有职工700多人，设有5个下属门诊部，年门诊量超过100万人次，年住院病人2万多人。</p>　　  
       <p style="line-height:30px;text-indent:2em">医院拥有教授等一大批高、中级专业技术人才，配备了国内领先水平的飞利浦1.5T磁共振仪、美国GE螺旋CT机，飞利浦数字化X光机、日本柯尼卡CR机、柯达DR机、奥林巴斯全自动生化仪、飞利浦iu22实时三维彩超、美国爱尔康白内障超声乳化仪、奥林巴斯腹腔镜及胃肠镜等一批先进医疗设备。</p>
       <p style="line-height:30px;text-indent:2em">医院设有：急诊科、内科（内一科、内二科）、外科（外一科、外二科）、妇产科、儿科、NICU、手外科、泌尿外科、神经外科、ICU、五官科、中医康复科、手术室、麻醉科、口腔科、皮肤科、功能检查、检验科科，影像科等科室。拥有国际标准的千级、万级层流手术室，能够开展一批难度较大的专科新技术。</p>
       <p style="line-height:30px;text-indent:2em">医院以救死扶伤为已任，以社会效益为目标，竭诚为人民群众提供优质的医疗服务，先后被评为广东省：“文明单位”、 “文明窗口”、“百家文明医院”、“巾帼文明示范岗”和东莞市“文明单位”、 “文明示范单位”、“文明单位标兵”等荣誉称号。</p>
      </p>
      </div>
      <div class="picture-display">
        <ul>
          <li><img src="../logo/picture1.jpg" width="300px" height="200px"></li>
          <li><img src="../logo/picture2.jpg" width="300px" height="200px"></li>
          <li><img src="../logo/picture3.jpg" width="300px" height="200px"></li>
          <li><img src="../logo/picture4.jpg" width="300px" height="200px"></li>
        </ul>
      </div>
      </el-tab-pane> -->
      <el-tab-pane label="就医指南" name="second">
      <div class="theme">
        <img src="../logo/AnYi.logo.jpg" width="50px" height="50px">
        <span class="span_font">就医指南</span>
      </div>
      <el-steps :space="100" direction="vertical" :active="1">
        <el-step title="步骤 1 " description="—— 材料准备-做好看病需要的材料，比如身份证，足够的现金。">
        </el-step>
        <el-step title="步骤 2" description="—— 挂号"></el-step>
        <el-step title="步骤 3" description="—— 门诊部-挂号之后，有的会让你等待，通知你去哪个门诊部看病。找相关的医生给你诊断治疗。"></el-step>
        <el-step title="步骤 4" description="—— 收费站-在门诊部"></el-step>
        <el-step title="步骤 5" description="—— 开药治疗-拿到报告单之后，给给你看病的医生查看。门诊部的医生根据你的报告单做出合适的治疗措施，当然如一些需要做手术之类的要经过你的同意方可进行。普通疾病的话会给你开药治疗等。">
        </el-step>
        <el-step title="步骤 6" description="—— 药房取药-医生已经开好了药单，到收费处同样要先缴费才能取药。把药单给收费员之后，去药房取药。">
        </el-step>
        <el-step title="步骤 7" description="—— 定期复查-为了你的身体健康，医生建议你复查的就去复查，按医生的叮嘱按时吃药，定期复查。有任何问题可拨打医院的服务热线。">
        </el-step>
      </el-steps>
      </el-tab-pane>
      <!-- <el-tab-pane label="科室导航" name="third">
      <div class="theme">
        <img src="../logo/AnYi.logo.jpg" width="50px" height="50px">
        <span class="span_font">科室导航</span>
      </div>
      <div class="card">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span style="line-height: 36px;">非手术科室</span>
            <el-button style="float: right;" type="primary" @click="check1">查看更多</el-button>
          </div>
          <div v-for="o in items1" :key="o" class="text item">
            {{ o }}
          </div>
        </el-card>
      </div>
      <div class="card">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span style="line-height: 36px;">手术科室</span>
            <el-button style="float: right;" type="primary" @click="check2">查看更多</el-button>
          </div>
          <div v-for="o in items2" :key="o" class="text item">
            {{ o }}
          </div>
        </el-card>
      </div>
      <div class="card">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span style="line-height: 36px;">诊断相关科室</span>
            <el-button style="float: right;" type="primary" @click="check3">查看更多</el-button>
          </div>
          <div v-for="o in items3" :key="o" class="text item">
            {{ o }}
          </div>
        </el-card>
      </div>
      </el-tab-pane> -->
      <el-tab-pane label="心理测试" name="fourth">
      <div class="theme">
        <img src="../logo/AnYi.logo.jpg" width="50px" height="50px">
        <span class="span_font">心理测试</span>
      </div>
      <div class="culture">
        <span style="font-size:30px;color:#75604F">心理测评流程以及注意事项</span>
        <p style="text-indent:4em">
          90项症状清单(Symptom Checklist 90,SCL-90)，又名症状自评量表(Self-reporting Inventory)，有时也叫做Hopkin's症状清单(HSCL，编制年代早于SCL-90，作者为同一人，HCSL最早版编于1954年)。于1975年编制，其作者是德若伽提斯(L.R.Derogatis)。该量表共有90个项目，包含有较广泛的精神病症状学内容，从感觉、情感、思维、意识、行为直至生活习惯、人际关系、饮食睡眠等，均有涉及，并采用10个因子分别反映10个方面的心理症状情况。<br/></p>
        <p style="text-indent:3em;font-size:20px;font-weight: 700;">
          SCL-90的每一个项目均采用5级评分制，具体如下:(1)没有:自觉无该项问题;(2)很轻，自觉有该项症状，但对被试者并无实际影响，或者影响轻微;(3)中度:自觉有该项症状，对被试者有一定影响;(4)偏重:自觉有该项症状，对被试者有相当程度的影响;(5)严重:自觉该症状的频度和强度都十分严重，对被试者的影响严重。<br/></p>
        <p style="text-indent:4em">
          这里的"影响"包括症状所致的痛苦和烦恼，也包括症状造成的心理社会功能损害。"轻、中、重"的具体定义，由被试者自己体会，不必做硬性规定。评定的时间，是"现在"或者是"最近一个星期"的实际感觉。<br/></p>
      </div>
      <div class="culture">
         <span style="font-size:40px;color:#75604F">请同学们仔细阅读注意事项 再进行测试</span>
         <div @click="toRescue">
           <span style="font-size:50px;font-weight: 750">心理测评链接</span></div>
         
         
      </div>
      </el-tab-pane>
    </el-tabs>

    <div class="dialog1">
      <el-dialog title="非手术科" :visible.sync="dialogVisible1" size="tiny" :before-close="handleClose">
        <div v-for="i in dialog1" :key="i">{{ i }}</div>
      </el-dialog>
    </div>
    <div class="dialog">
      <el-dialog title="手术科" :visible.sync="dialogVisible2" size="tiny" :before-close="handleClose">
        <div v-for="i in dialog2" :key="i">{{ i }}</div>
      </el-dialog>
    </div>
    <div class="dialog">
      <el-dialog title="诊断相关科室" :visible.sync="dialogVisible3" size="tiny" :before-close="handleClose">
        <div v-for="i in dialog3" :key="i">{{ i }}</div>
      </el-dialog>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data () {
      return {
        activeName: 'second',
        dialogVisible1: false,
        dialogVisible2: false,
        dialogVisible3: false,
        items1: ['内科学系', '心内科', '呼吸内科', '消化内科', '肾内科'],
        items2: ['外科学系', '基本外科', '骨科', '心外科', '胸外科'],
        items3: ['超声医学科', '病理科', '检验科', '放射科', '放射治疗科'],
        dialog1: ['血液内科', '风湿免疫科', '感染内科', '普通内科', '肿瘤内科', '内科ICU', '内分泌科', '肠外肠内营养科', '重症医学科(ICU)', '儿科', '神经科', '心理医学科', '皮肤科', '变态（过敏）反应科', '急诊科', '中医科', '老年医学科'],
        dialog2: ['泌尿外科', '神经外科', '血管外科', '乳腺外科', '肝脏外科', '妇产科', '眼科', '耳鼻喉科', '口腔科', '麻醉科'],
        dialog3: ['核医学科', '营养科', '输血科', '药剂科', '病案科', '物理医学康复科', '疾病分类中心'],
        url: 'https://www.apesk.com/SCL90/'
      };
    },
    methods: {
      handleClick (tab, event) {
        console.log(tab, event);
      },
      // 查看更多
      check1 () {
        this.dialogVisible1 = true;
      },
      check2 () {
        this.dialogVisible2 = true;
      },
      check3 () {
        this.dialogVisible3 = true;
      },
      handleClose (done) {
        this.$confirm('确认关闭？')
          .then(_ => {
            done();
          })
          .catch(_ => {});
      },
      toRescue () {
        window.location.href = this.url;
      }
    }
  };
  
</script>

<style lang="stylus-loader" rel="stylesheet/stylus">
  .psychologicalTest .span_font
    font-size:24px
    color:blue
  .psychologicalTest .introduction
    width:700px
    height:550px
    float:left
    position:relative
    margin-top:50px
  .psychologicalTest .picture-display
    float:right
    width:600px
    height:500px
  .psychologicalTest .picture-display ul li
    float:left
    margin-top:50px
  .psychologicalTest .card
    float:left
    margin-top:50px
    padding-left:20px
  .psychologicalTest .text
    font-size:14px
  .psychologicalTest .item
    padding:18px 0
  .psychologicalTest .clearfix:before, .clearfix:after
    display: table
    content: ""
  .psychologicalTest .clearfix:after
    clear: both
  .psychologicalTest .box-card
    width: 420px
    background:green
  .psychologicalTest .culture
    margin:auto
    margin-top:50px
    width:500px 
    padding-left:150px
    float:left
</style>