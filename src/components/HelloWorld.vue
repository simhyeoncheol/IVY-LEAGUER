<template>
  <div class="wrap">
    <div class="menuDiv">
      <div class="header">
        <div id="logoId" @click="pagechang(1)">IVY LEAGUER</div>
        <div id="serchBtnBoxId">
          <input
            type="text"
            id="searchinp"
            placeholder="검색어를 입력해 주세요"
          />
          <div id="serchBtnId" @click="serchBtn()">
            <img class="searchIcon" src="/imgs/searchIcon.png" />
          </div>
          <img src="" alt="" />
        </div>
      </div>
      <div class="underMenu menu">
        <div class="menu">
          <div class="menuItem">
            <a class="mainMenu"
              ><img src="/imgs/menu_FILL0_wght400_GRAD0_opsz24.png"
            /></a>
          </div>
          <div class="menuItem">
            <a @click="pagechang(2)" class="mainMenu">채용정보</a>
          </div>
          <div class="menuItem">
            <a @click="pagechang(3)" class="mainMenu">인재풀</a>
          </div>
          <div class="menuItem"><a class="mainMenu">이력서</a></div>
        </div>
        <div class="menu">
          <div class="menuItem"><a class="login">로그인</a></div>
          <div class="menuItem">
            <a class="login">회원가입</a>
          </div>
          <div class="menuItem"><a class="login">기업회원</a></div>
        </div>
      </div>
    </div>
    <div v-if="page === 1">
      <div class="body">
        <div class="imgWrap" style="display: contents">
          <div class="imgDiv">
            <img src="/imgs/resume.png" alt="" class="img" />
          </div>
          <div class="btnDiv"><button class="btn">이력서 작성하기</button></div>
        </div>
        <div class="boxWrap" style="margin-left: 40px">
          <div style="display: flex; height: 50%">
            <div class="box" style="margin-right: 30px; width: 100%">
              <div class="textDiv">
                <div class="title">이력서 점수</div>
                <div style="display: flex; justify-content: space-around">
                  <img
                    id="comparison"
                    src="/imgs/KakaoTalk_Photo_2023-11-17-06-31-36.png"
                  />
                </div>
                <div style="justify-content: center; display: flex">
                  <button class="btnResume">이력서 업데이트</button>
                </div>
              </div>
            </div>

            <div class="box" style="width: 60%">
              <div class="textDiv">
                <div class="title">채용 내역</div>
                <div class="recruitTextDiv">
                  지원한 기업
                  <p style="color: green">(?)</p>
                </div>
                <div class="recruitTextDiv">
                  받은 입사 제안
                  <p style="color: green">(?)</p>
                </div>
                <div class="recruitTextDiv">
                  이력서 열람 기관
                  <p style="color: green">(?)</p>
                </div>
                <div class="recruitTextDiv">
                  업데이트 알림
                  <p style="color: green">(?)</p>
                </div>
              </div>
            </div>
          </div>

          <div class="box" style="width: 100%; height: 49%; padding: 16px">
            <div class="title">채용 인사이트</div>
            <div class="recruit" style="height: 25%">
              <div class="border" style="width: 100%">
                <div class="recruitTextDiv">신한은행</div>
                <div style="font-size: large; font-weight: bold">
                  2023 하반기 신입사원 채용
                </div>
              </div>
              <div class="recruitItem">15일 남은</div>
              <div class="recruitItem recruitItemGreen">안정</div>
            </div>
            <div class="recruit2" style="height: 25%">
              <div class="border border2" style="width: 100%">
                <div class="plus">
                  <p class="plusIcon">+</p>
                </div>
              </div>
            </div>
            <div class="recruit2" style="height: 25%">
              <div class="border border2" style="width: 100%">
                <div class="plus">
                  <p class="plusIcon">+</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div id="card">
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-8.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">(주)삼성</div>
            <div id="cardPostName">(주)삼성전자 웹개발자 채용 공고</div>
            <div id="cardDDay">D-15</div>
          </div>
        </div>
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-7.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">HANSSEM</div>
            <div id="cardPostName">HANSSEM 실내 디자이너 채용 공고</div>
            <div id="cardDDay">D-10</div>
          </div>
        </div>
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-6.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">하나은행</div>
            <div id="cardPostName">하나은행 본점 은행원 채용 공고</div>
            <div id="cardDDay">D-01</div>
          </div>
        </div>
      </div>
      <div id="card">
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-9.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">대웅제약</div>
            <div id="cardPostName">대웅제약 경비원 채용 공고</div>
            <div id="cardDDay">D-20</div>
          </div>
        </div>
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-2.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">대림산업</div>
            <div id="cardPostName">대림산업 개발자 채용 공고</div>
            <div id="cardDDay">D-17</div>
          </div>
        </div>
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-3.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">KBS</div>
            <div id="cardPostName">KBS PD채용 공고</div>
            <div id="cardDDay">D-18</div>
          </div>
        </div>
      </div>
      <div id="card">
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-50-1.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">비씨카드</div>
            <div id="cardPostName">비씨카드 영원사원 채용 공고</div>
            <div id="cardDDay">D-19</div>
          </div>
        </div>
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-52-4.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">동양</div>
            <div id="cardPostName">동양 해외파견직 채용 공고</div>
            <div id="cardDDay">D-07</div>
          </div>
        </div>
        <div id="companyCard">
          <div id="cardLogo">
            <img
              id="imgs"
              src="/imgs/KakaoTalk_Photo_2023-11-16-23-42-51-5.png"
            />
          </div>

          <div id="cardInfo">
            <div id="companyCardTitle">the 겔러리아</div>
            <div id="cardPostName">the 겔러리아 사진작가 채용 공고</div>
            <div id="cardDDay">D-09</div>
          </div>
        </div>
      </div>
    </div>

    <div class="page2" v-if="page === 2">
      <div id="menuLeft" style="margin-right: 30px">
        <div class="LeftDiv">
          <div class="title">경력</div>
          <div style="display: flex; justify-content: center">
            <div class="">
              <select name="as" id="" class="select">
                <option disabled selected>선택</option>
                <option value="">무관</option>
                <option value="">1년차</option>
                <option value="">2년차</option>
                <option value="">3년차</option>
                <option value="">5년차</option>
                <option value="">6년차</option>
                <option value="">9년차</option>
                <option value="">10년차</option>
                <option value="">11년차</option>
                <option value="">12년차</option>
                <option value="">13년차</option>
                <option value="">14년차</option>
                <option value="">15년차</option>
                <option value="">16년차</option>
                <option value="">17년차</option>
                <option value="">18년차</option>
              </select>
              ~
              <select name="" id="" placeholder="선택" class="select">
                <option disabled selected>선택</option>
                <option value="">무관</option>
                <option value="">1년차</option>
                <option value="">2년차</option>
                <option value="">3년차</option>
                <option value="">5년차</option>
                <option value="">6년차</option>
                <option value="">9년차</option>
                <option value="">10년차</option>
                <option value="">11년차</option>
                <option value="">12년차</option>
                <option value="">13년차</option>
                <option value="">14년차</option>
                <option value="">15년차</option>
                <option value="">16년차</option>
                <option value="">17년차</option>
                <option value="">18년차</option>
              </select>
            </div>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">지역</div>
          <div class="leftBorder">
            <p class="">강원도</p>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">직무</div>
          <div class="leftBorder">
            <p class="">웹 개발자</p>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">학력</div>
          <div class="" style="justify-content: center; display: grid">
            <div>
              <input type="radio" name="edu" />고등학교
              <input type="radio" name="edu" />대학(4년)
              <input type="radio" name="edu" />박사
            </div>
            <div style="margin-top: 5px">
              <input type="radio" name="edu" />대학(2,3년)
              <input type="radio" name="edu" />석사
            </div>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">연봉</div>
          <div style="display: flex; justify-content: center">
            <div class="">
              <select name="as" id="" class="select">
                <option disabled selected>선택</option>
                <option value="">무관</option>
                <option value="">1000</option>
              </select>
              ~
              <select name="" id="" placeholder="선택" class="select">
                <option disabled selected>선택</option>
                <option value="">무관</option>
                <option value="">4000</option>
              </select>
            </div>
          </div>
        </div>
      </div>
      <div id="menuRight">
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now">현재 지원자 <span id="number">104</span> 명 </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img
                        id="flagSize"
                        src="/imgs/free-icon-united-states-206626.png"
                    /></span>
                    <span id="ListName">삼성전자</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName">삼성SDI 반도체 품질검사 구인</span>
                    </div>

                    <div id="thirdtLine">
                      <span>미국ㆍ신소재공학과 관련 전공 대학교 졸업</span>
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>면접 후 결정</div>
                  <div>[계약직] 12개월</div>
                  <div>D-10비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 409 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 2003 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: red">86점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now">현재 지원자 <span id="number">559</span> 명 </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img
                        id="flagSize"
                        src="/imgs/free-icon-vietnam-2151393.png"
                    /></span>
                    <span id="ListName">삼성전자</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName"
                        >삼성전자 임베디드 연수고 개발자 구인</span
                      >
                    </div>

                    <div id="thirdtLine">
                      <span
                        >베트남(한국어가능)ㆍ기계관련전공 | 성실한분 구함</span
                      >
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>면접 후 결정</div>
                  <div>[정규직]</div>
                  <div>D-10비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 1123 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 10087 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: blue">78점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now">현재 지원자 <span id="number">123</span> 명 </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img
                        id="flagSize"
                        src="/imgs/free-icon-vietnam-2151393.png"
                    /></span>
                    <span id="ListName">현대자동차</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName">자동차 마케팅, 영업사원 구직</span>
                    </div>

                    <div id="thirdtLine">
                      <span>베트남ㆍ자동차판매 경험자 구함</span>
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>면접 후 결정</div>
                  <div>[계약직] 12개월</div>
                  <div>D-10비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 1224 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 300 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: blue">76점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now"
                >현재 지원자 <span id="number">1424</span> 명
              </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img
                        id="flagSize"
                        src="/imgs/free-icon-canada-206609.png"
                    /></span>
                    <span id="ListName">한국전력공사</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName">성남시 전봇대 수리기사 구인</span>
                    </div>

                    <div id="thirdtLine">
                      <span>캐나다ㆍ전기 | 전자 석사 졸업</span>
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>면접 후 결정</div>
                  <div>[계약직] 12개월</div>
                  <div>D-10비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 2009 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 145 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: blue">70점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now">현재 지원자 <span id="number">561</span> 명 </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img id="flagSize" src="/imgs/free-icon-china-206818.png"
                    /></span>
                    <span id="ListName">더본코리아</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName"
                        >중화요리 기술 연구소 연구원 모집</span
                      >
                    </div>

                    <div id="thirdtLine">
                      <span>중국ㆍ중국요리전문대학 졸업</span>
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>3,000</div>
                  <div>[계약직] 3개월</div>
                  <div>D-2비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 409 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 3 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: yellow">68점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now">현재 지원자 <span id="number">201</span> 명 </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img id="flagSize" src="/imgs/free-icon-china-206818.png"
                    /></span>
                    <span id="ListName">알바몬</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName">외국인 고객 상담원 구인</span>
                    </div>

                    <div id="thirdtLine">
                      <span>중국ㆍ영어가능자</span>
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>200</div>
                  <div>[계약직] 3개월</div>
                  <div>D-2비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 799 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 321 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: yellow">62점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <span id="now">현재 지원자 <span id="number">15</span> 명 </span>
              <div id="line"></div>
              <div style="display: flex">
                <div style="margin-right: auto">
                  <div id="firstLine">
                    <span id="ListFlag">
                      <img
                        id="flagSize"
                        src="/imgs/free-icon-germany-206690.png"
                    /></span>
                    <span id="ListName">에버랜드</span>
                  </div>
                  <div id="subTitle">
                    <div id="secondtLine">
                      <span id="postName">호랑이, 곰돌이, 펭귄, 수달 관리</span>
                    </div>

                    <div id="thirdtLine">
                      <span>독일 사육사학과전문대학 졸업</span>
                    </div>
                  </div>
                </div>
                <div id="companyListMidItem">
                  <div>320</div>
                  <div>[계약직] 6개월</div>
                  <div>D-2비자</div>
                </div>
                <div
                  id="companyListRightItem"
                  style="margin-right: 20px; align-self: center"
                >
                  <div>
                    <img
                      src="/imgs/visibility_FILL0_wght400_GRAD0_opsz24.png"
                    /><span id="number"> 112 </span><span>명</span>
                  </div>
                  <div>
                    <img
                      src="/imgs/volunteer_activism_FILL0_wght400_GRAD0_opsz24.png"
                    /><span>스크랩</span><span id="number"> 32 </span
                    ><span>명</span>
                  </div>
                  <div id="line"></div>
                  <div id="scoreArea">
                    <div id="machingScore">[매칭접수]</div>
                    <div id="score" style="color: yellow">50점</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="page2" v-if="page === 3">
      <div id="menuLeft" style="margin-right: 30px">
        <div class="LeftDiv">
          <div class="title">경력</div>
          <div style="display: flex; justify-content: center">
            <div class="">
              <select name="as" id="" class="select">
                <option disabled selected>선택</option>
                <option value="">무관</option>
                <option value="">1년차</option>
                <option value="">2년차</option>
                <option value="">3년차</option>
                <option value="">5년차</option>
                <option value="">6년차</option>
                <option value="">9년차</option>
                <option value="">10년차</option>
                <option value="">11년차</option>
                <option value="">12년차</option>
                <option value="">13년차</option>
                <option value="">14년차</option>
                <option value="">15년차</option>
                <option value="">16년차</option>
                <option value="">17년차</option>
                <option value="">18년차</option>
              </select>
              ~
              <select name="" id="" placeholder="선택" class="select">
                <option disabled selected>선택</option>
                <option value="">무관</option>
                <option value="">1년차</option>
                <option value="">2년차</option>
                <option value="">3년차</option>
                <option value="">5년차</option>
                <option value="">6년차</option>
                <option value="">9년차</option>
                <option value="">10년차</option>
                <option value="">11년차</option>
                <option value="">12년차</option>
                <option value="">13년차</option>
                <option value="">14년차</option>
                <option value="">15년차</option>
                <option value="">16년차</option>
                <option value="">17년차</option>
                <option value="">18년차</option>
              </select>
            </div>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">지역</div>
          <div class="leftBorder">
            <p class="">강원도</p>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">직무</div>
          <div class="leftBorder">
            <p class="">웹 개발자</p>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">학력</div>
          <div class="" style="justify-content: center; display: grid">
            <div>
              <input type="radio" name="edu" />고등학교
              <input type="radio" name="edu" />대학(4년)
              <input type="radio" name="edu" />박사
            </div>
            <div style="margin-top: 5px">
              <input type="radio" name="edu" />대학(2,3년)
              <input type="radio" name="edu" />석사
            </div>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">국적</div>
          <div class="leftBorder">
            <p class="">미국</p>
          </div>
        </div>
        <div class="LeftDiv">
          <div class="title">비자</div>
          <div class="leftBorder">
            <p class="">D-10</p>
          </div>
        </div>
      </div>
      <div id="menuRight">
        <div id="companyList">
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <div style="display: flex; justify-content: space-between">
                <div style="width: -webkit-fill-available">
                  <div id="firstLine" style="display: flex">
                    <div id="" style="height: 100%">
                      <img
                        id="flagSize"
                        src="/imgs/KakaoTalk_20231117_065247295_01.png"
                        style="width: 6%"
                      />
                    </div>
                    <div id="ListName">스티븐 무함마드</div>
                    <ul style="display: flex">
                      <li class="list">30대 초반</li>
                      <li class="list">경력 8년 2개월</li>
                    </ul>
                  </div>
                  <div style="margin-left: 15%; margin-top: 10px">영리법인</div>
                  <div style="margin-left: 15%">
                    서울 소재 2,3년제 대학교 (졸업)
                  </div>
                  <div
                    style="margin-left: 15%; display: flex; margin-top: 10px"
                  >
                    <div class="skills" style="color: blue; font: bold">
                      VISA D-10
                    </div>
                    <div class="skills">Topik 4급</div>
                    <div class="skills">영업관리</div>
                    <div class="skills">가맹점관리</div>
                    <div class="skills">거래처관리</div>
                  </div>
                </div>

                <div
                  id="companyListRightItem"
                  style="
                    margin-right: 20px;
                    align-self: center;
                    width: 30%;
                    text-align: center;
                  "
                >
                  <div>
                    <div id="machingScore">매칭점수</div>
                    <div id="score" style="color: red">86점</div>
                  </div>
                  <button class="proposalBtn">면접 제안하기</button>
                </div>
              </div>
            </div>
          </div>

          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <div style="display: flex; justify-content: space-between">
                <div style="width: -webkit-fill-available">
                  <div id="firstLine" style="display: flex">
                    <div id="" style="height: 100%">
                      <img
                        id="flagSize"
                        src="/imgs/KakaoTalk_20231117_065247295.png"
                        style="width: 6%"
                      />
                    </div>
                    <div id="ListName">실리안 음뷔페</div>
                    <ul style="display: flex">
                      <li class="list">20대 후반</li>
                      <li class="list">경력 5년 3개월</li>
                    </ul>
                  </div>
                  <div style="margin-left: 15%; margin-top: 10px">영리법인</div>
                  <div style="margin-left: 15%">
                    프랑스 국립대학 4년제 (졸업)
                  </div>
                  <div
                    style="margin-left: 15%; display: flex; margin-top: 10px"
                  >
                    <div class="skills" style="color: blue; font: bold">
                      VISA D-10
                    </div>
                    <div class="skills">Topik 3급</div>
                    <div class="skills">제조업</div>
                    <div class="skills">사육사학과</div>
                  </div>
                </div>

                <div
                  id="companyListRightItem"
                  style="
                    margin-right: 20px;
                    align-self: center;
                    width: 30%;
                    text-align: center;
                  "
                >
                  <div>
                    <div id="machingScore">매칭점수</div>
                    <div id="score" style="color: blue">77점</div>
                  </div>
                  <button class="proposalBtn">면접 제안하기</button>
                </div>
              </div>
            </div>
          </div>
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <div style="display: flex; justify-content: space-between">
                <div style="width: -webkit-fill-available">
                  <div id="firstLine" style="display: flex">
                    <div id="" style="height: 100%">
                      <img
                        id="flagSize"
                        src="/imgs/KakaoTalk_20231117_065247295_03.png"
                        style="width: 6%"
                      />
                    </div>
                    <div id="ListName">안졸리나 졸리나</div>
                    <ul style="display: flex">
                      <li class="list">20대 후반</li>
                      <li class="list">경력 2년</li>
                    </ul>
                  </div>
                  <div style="margin-left: 15%; margin-top: 10px">영리법인</div>
                  <div style="margin-left: 15%">홍콩대학교 4년제 (졸업)</div>
                  <div
                    style="margin-left: 15%; display: flex; margin-top: 10px"
                  >
                    <div class="skills" style="color: blue; font: bold">
                      VISA D-2
                    </div>
                    <div class="skills">Topik 4급</div>
                    <div class="skills">경영학과</div>
                    <div class="skills">경영 보조</div>
                  </div>
                </div>

                <div
                  id="companyListRightItem"
                  style="
                    margin-right: 20px;
                    align-self: center;
                    width: 30%;
                    text-align: center;
                  "
                >
                  <div>
                    <div id="machingScore">매칭점수</div>
                    <div id="score" style="color: blue">73점</div>
                  </div>
                  <button class="proposalBtn">면접 제안하기</button>
                </div>
              </div>
            </div>
          </div>
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <div style="display: flex; justify-content: space-between">
                <div style="width: -webkit-fill-available">
                  <div id="firstLine" style="display: flex">
                    <div id="" style="height: 100%">
                      <img
                        id="flagSize"
                        src="/imgs/KakaoTalk_20231117_065247295_04.png"
                        style="width: 6%"
                      />
                    </div>
                    <div id="ListName">휘트니 스턴</div>
                    <ul style="display: flex">
                      <li class="list">20대 초반</li>
                      <li class="list">신입</li>
                    </ul>
                  </div>
                  <div style="margin-left: 15%; margin-top: 10px">해당없음</div>
                  <div style="margin-left: 15%">
                    강릉 소재 2,3년제 대학교 (졸업)
                  </div>
                  <div
                    style="margin-left: 15%; display: flex; margin-top: 10px"
                  >
                    <div class="skills" style="color: blue; font: bold">
                      VISA D-2
                    </div>
                    <div class="skills">Topik 5급</div>
                    <div class="skills">기계공학과</div>
                  </div>
                </div>

                <div
                  id="companyListRightItem"
                  style="
                    margin-right: 20px;
                    align-self: center;
                    width: 30%;
                    text-align: center;
                  "
                >
                  <div>
                    <div id="machingScore">매칭점수</div>
                    <div id="score" style="color: blue">65점</div>
                  </div>
                  <button class="proposalBtn">면접 제안하기</button>
                </div>
              </div>
            </div>
          </div>
          <div id="textarea">
            <div id="companyListLeftItem" style="width: 100%">
              <div style="display: flex; justify-content: space-between">
                <div style="width: -webkit-fill-available">
                  <div id="firstLine" style="display: flex">
                    <div id="" style="height: 100%">
                      <img
                        id="flagSize"
                        src="/imgs/KakaoTalk_20231117_065247295_02.png"
                        style="width: 6%"
                      />
                    </div>
                    <div id="ListName">응우옌 니꼴라스</div>
                    <ul style="display: flex">
                      <li class="list">30대 초반</li>
                      <li class="list">신입</li>
                    </ul>
                  </div>
                  <div style="margin-left: 15%; margin-top: 10px">해당없음</div>
                  <div style="margin-left: 15%">
                    베트남 국립대학 4년제 (졸업)
                  </div>
                  <div
                    style="margin-left: 15%; display: flex; margin-top: 10px"
                  >
                    <div class="skills" style="color: blue; font: bold">
                      VISA D-2
                    </div>
                    <div class="skills">Topik 2급</div>
                    <div class="skills">컴퓨터공학과</div>
                    <div class="skills">풀스택 웹개발자</div>
                  </div>
                </div>

                <div
                  id="companyListRightItem"
                  style="
                    margin-right: 20px;
                    align-self: center;
                    width: 30%;
                    text-align: center;
                  "
                >
                  <div>
                    <div id="machingScore">매칭점수</div>
                    <div id="score" style="color: yellow">59점</div>
                  </div>
                  <button class="proposalBtn">면접 제안하기</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  components: {},
  data() {
    return {
      page: 1,
    };
  },
  methods: {
    serchBtn() {
      console.log("12312");
    },
    pagechang(num) {
      this.page = num;
    },
  },
};
</script>

<style lang="scss">
#comparison {
  width: 220px;
  height: 90px;
}
.skills {
  background: #367c682b;
  color: #7d7d7d;
  border-radius: 4px;
  padding: 2px;
  margin-right: 6px;
}
.proposalBtn {
  border: 1.5px solid green;
  border-radius: 6px;
  padding: 6px 15px;
  font-size: 17px;
  font-weight: 600;
}
.listen {
  border-radius: 25px;
  background: #00d3ab;
  color: white;
  padding-left: 6px;
  padding-right: 6px;
  font-weight: bold;
}
.list {
  margin-right: 25px;
  color: gray;
}
#ListFlag {
  width: 100%;
  height: 100%;
}
#companyList {
  margin-bottom: 3%;
}

#machingScore {
  font-size: 12px !important;
  font-weight: 700;
}
#scoreArea {
  text-align: center;
  font-size: 20px;
}

#companyListRightItem {
  text-align: right;
}

#companyListMidItem {
  margin-right: 13%;
  align-self: center;
  text-align: center;
}
#subTitle {
  margin-top: 10%;
}
#score {
  color: red;
  font-size: 30px;
  font-weight: 700;
  -webkit-text-stroke: 1.5px black;
}

#textarea {
  border: 1px solid #00000030;
  display: flex;
}

#firstLine {
  margin-top: 3%;

  align-content: center;
}

#ListName {
  margin-left: 15%;
  font-size: 17px;
  font-weight: 600;
}

#flagSize {
  width: 3%;
  position: absolute;
}

#number {
  color: red;
}

#line {
  margin: 5px 0px;
  width: 100%;
  border: 0.5px solid black;
  justify-content: center;
}

#thirdtLine {
  margin-top: 4px;
  color: blue;
}
#secondtLine {
  margin-top: 10px;
  width: 400px;
}
#postName {
  font-size: 20px;
  font-weight: 700;
}

#companyListLeftItem {
  padding: 15px;
}
[type="radio"] {
  appearance: none;
  width: 20px;
  height: 20px;
  border: 1px solid #0080004a;
  border-radius: 4px;
}
.page2 {
  display: flex;
  height: 100%;
  margin-right: 5%;
  margin-left: 5%;
  justify-content: center;
}

[type="radio"] {
  appearance: none;
  width: 20px;
  height: 20px;
  border: 1px solid #0080004a;
  border-radius: 4px;
}

[type="radio"]:checked {
  background-color: #367c68;
}

.leftBorder {
  border: 1px solid #cccc;
  border-radius: 5px;
  text-align: center;
}

.leftBorder > p {
  margin: 10px !important;
  color: gray;
  font-size: 16px;
  font-weight: bold;
}

.LeftDiv {
  margin-bottom: 20px;
}

.select {
  width: 100px;
  border: 1px solid #367c68;
  border-radius: 4px;
  padding: 9px 13px;
  font-weight: 400;
  font-size: 16px;
  line-height: 16px;
  margin-bottom: 2px;
}

.select option {
  padding: 3px 0;
}

#menuRight {
  margin-bottom: auto;
  width: 70%;
  border: 1px solid #0000003d;
  border-radius: 6px;
  box-shadow: 4px 4px 8px 1px #cccc;
}

#menuLeft {
  height: fit-content;
  width: 30%;
  position: relative;
  border: 1px solid #0000003d;
  padding: 15px;
  border-radius: 6px;
  box-shadow: 4px 4px 8px 1px #cccc;
}

.header {
    width: 100%;
    display: flex;
    /* text-align: center; */
    padding: 30px;
    justify-content: center;
}

.menuDiv {
  box-shadow: 0px -9px 20px 1px gray;
  margin-bottom: 40px;
}

#logoId {
  position: absolute;
    left: 19px;
    font-weight: 600;
    color: #367c68;
    margin-right: 30px;
    font-size: xx-large;
}

#serchBtnBoxId {

    width: 30%;
    /* text-align: center; */
    height: 45px;
    border: 3px solid #367c68;
    border-radius: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: stretch;
    flex-wrap: nowrap;
    flex-direction: row;

}

#serchBtnId {
  padding: 3px;
}

#searchinp {
  width: 100%;
  height: 100%;
  padding-left: 15px;
}

.searchIcon {
  padding: 4px;
}

.body {
  width: 90%;
  display: flex;
  margin-left: 5%;
  margin-right: 5%;
}

.menu {
  display: flex;
}

.underMenu {
  justify-content: space-between;
  padding-left: 30px;
  padding-right: 30px;
  padding-bottom: 15px;
}

.menuItem {
  margin-right: 10px;
}

.login {
  color: #7c7575 !important;
  font-weight: 600;
}

.mainMenu {
  color: black !important;
  font-weight: 600;
}

.img {
  width: 100%;
  border-radius: 6px;
}

.imgDiv {
  width: 100%;
}

.imgWrap {
  width: 50%;
}

.btnDiv {
  position: absolute;
  top: 440px;
  left: 120px;
}

.btn {
  border: 1px solid #367c68;
  background-color: #367c68;
  color: white;
  font-size: 15px;
  font-weight: 600;
  border-radius: 3px;
  padding: 10px;
}

.box {
  box-shadow: 0px 1px 20px 0px #80808045;
  border-radius: 5px;
  margin-bottom: 30px;
}

.boxWrap {
  width: 100%;
}

.title {
  font-size: larger !important;
  font-weight: bold !important;
}

.textDiv {
  margin: 5%;
}

#imgs {
  width: 70%;
  height: 100%;
}

#cardInfo {
  padding: 10px;
}

#companyCardTitle {
  font-weight: 700;
  font-size: 15px;
}

#cardPostName {
  font-size: 20px;
  font-weight: bolder;
}

#cardDDay {
  font-size: 12px;
  padding: 3px;
  color: red;
}

#cardLogo {
  text-align: center;

  align-content: center;
  width: 100%;
  height: 50%;
}

#card {
  margin-left: 5%;
  margin-right: 5%;
  justify-content: space-between;
  display: flex;
  position: relative;
}

#companyCard {
  width: 380px;
  height: 200px;
  margin-top: 20px;
  border-radius: 10px;
  border-top: 5px solid #367c68;
  box-shadow: 1px 1px 5px;
}

.recruitTextDiv {
  display: flex;
  justify-content: space-between;
  color: gray;
}

.btnResume {
  margin-top: 15px;
  padding: 10px;
  border-radius: 6px;
  background-color: #f8f8f8;
  color: #367c68;
  font-weight: bold;
}

.recruit {
  display: flex;
  border: 1px solid gray;
  border-radius: 5px;
  margin-left: 3%;
  margin-right: 3%;
  margin-top: 5px;
  margin-bottom: 5px;
  padding-left: 15px;
  padding-right: 15px;
  padding-top: 3px;
  padding-bottom: 3px;
}

.recruit2 {
  display: flex;
  border: 1px solid gray;
  border-radius: 5px;
  margin-left: 3%;
  margin-right: 3%;
  margin-top: 5px;
  margin-bottom: 5px;
  padding-left: 15px;
  padding-right: 15px;
  padding-top: 3px;
  padding-bottom: 3px;
  height: 25%;
  background: #f8f8f8;
  border-style: dashed;
}

.recruitItem {
  align-self: center;
  width: 144px;
  display: flex;
  justify-content: center;
  border-radius: 22px;
  background: #7f8389;
  color: white;
  font-weight: 800;
}

.recruitItemGreen {
  width: 90px;
  background: #367c68;
  margin-left: 10px;
}

.border2 {
  width: 100%;
  align-items: center;
  display: grid;
}

.plus {
  align-items: center;
  display: flex;
  justify-content: center;
}

.plusIcon {
  height: 30px;
  margin-bottom: 0 !important;
  border: 1px solid;
  width: 30px;
  font-size: larger;
  border-radius: 30px;
  text-align: center;
  background: gray;
  color: white;
}
</style>