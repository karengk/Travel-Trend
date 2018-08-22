<html>
<head>
<title>Title of the document</title>
<style>
  body {
    background: #efefef;
    padding: 20px;
    font-family: Helvetica;
  }

  button {
    background: #0084ff;
    border: none;
    border-radius: 5px;
    padding: 8px 14px;
    font-size: 15px;
    color: #fff;
  }

</style>

<script>
  var $form = $('form#test-form'),
    url = 'https://script.google.com/macros/s/AKfycbw_4pK_SHeymLeDSxQpbmgSIG1q7oQMSJW66fvrTvlbufFtlT0/exec'

  $('#submit-form').on('click', function(e) {
    e.preventDefault();
    var jqxhr = $.ajax({
      url: url,
      method: "GET",
      dataType: "json",
      data: $form.serializeObject()
    }).success(
      // do something
    );
  })

</script>

</head>

<body>

<form id="selfmining">

  <div>
    <label>이름</label>
    <input type="text" name="name" placeholder="이름을 입력해 주세요" />
  </div>

  <div>
    <label>본부</label>
    <select name="hq">
      <option value="C-Level">C-Level</option>
      <option value="CGEX">CGEX</option>
      <option value="CEO직속">CEO직속</option>
      <option value="기술">기술</option>
      <option value="보안">보안</option>
      <option value="제품">제품</option>
      <option value="경영기획/운영">경영기획/운영</option>
      <option value="경영지원">경영지원</option>
      <option value="감사/리스크관리">감사/리스크관리</option>
    </select>
  </div>

  <div>
    <label>팀</label>
    <input type="text" name="team" placeholder="팀 이름을 입력해 주세요." />
  </div>

  <div>
    <label>Field 4</label>
    <input type="text" name="task1" placeholder="Task 1" />
  </div>

  <div>
    <button type="submit" id="submit-form">Submit</button>
  </div>

</form>

</body>

</html>
