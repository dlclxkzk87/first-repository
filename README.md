<h1 class="entry-title uk-margin-remove-top ui-display2">**마크 저커버그**가 직접 만들어 본 AI 비서 ‘자비스’</h1>
[200~<time class="entry-date published" datetime="2016-12-19T23:15:14+09:00">2016년 12월 19일</time>
[200~<div class="content uk-width-4-5@m uk-width-1-1@s">
		<p>지난 1월, Facebook CEO 마크 저커버그(Mark Zuckerberg)가 &lt;아이언맨&gt;에 등장하는 ‘자비스’와 같은 AI 비서 개발에 도전하겠다는 개인적인 새해 목표를 밝힌 것을 기억하시나요?</p>
<p>저커버그가 1년간의 도전의 결과물인 자비스를 모두에게 소개했습니다.</p>
<p>먼저, 저커버그가 자신의 Facebook 프로필(<a href="https://www.facebook.com/zuck" rel="nofollow" class="in_article_link">https://www.facebook.com/zuck</a>)에 업로드한 동영상으로 자비스를 만나 볼까요?</p>
<div class="fb-video fb_iframe_widget fb_iframe_widget_fluid_desktop" data-allowfullscreen="true" data-href="https://www.facebook.com/zuck/videos/10103351034741311/" style="width: 100%;" fb-xfbml-state="rendered" fb-iframe-plugin-query="allowfullscreen=true&amp;app_id=249643311490&amp;container_width=510&amp;href=https%3A%2F%2Fwww.facebook.com%2Fzuck%2Fvideos%2F10103351034741311%2F&amp;locale=ko_KR&amp;sdk=joey"><span style="vertical-align: bottom; width: 510px; height: 261px;"><iframe name="f367f4e4091bb4" width="1000px" height="1000px" data-testid="fb:video Facebook Social Plugin" title="fb:video Facebook Social Plugin" frameborder="0" allowtransparency="true" allowfullscreen="true" scrolling="no" allow="encrypted-media" src="https://www.facebook.com/v2.3/plugins/video.php?allowfullscreen=true&amp;app_id=249643311490&amp;channel=https%3A%2F%2Fstaticxx.facebook.com%2Fx%2Fconnect%2Fxd_arbiter%2F%3Fversion%3D46%23cb%3Df2b2e34d70b694%26domain%3Dabout.fb.com%26is_canvas%3Dfalse%26origin%3Dhttps%253A%252F%252Fabout.fb.com%252Ff33d182c3c2ea2%26relation%3Dparent.parent&amp;container_width=510&amp;href=https%3A%2F%2Fwww.facebook.com%2Fzuck%2Fvideos%2F10103351034741311%2F&amp;locale=ko_KR&amp;sdk=joey" style="border: none; visibility: visible; width: 510px; height: 261px;" class=""></iframe></span></div>
<p>&nbsp;</p>
<p>저커버그는 자비스 구축 과정에서 배우고 느낀 점을 글로 전하기도 했는데요, 아래에서 간략한 내용을 만나 보실 수 있습니다.</p>
<p>자비스는 어떻게 개발됐는지, 무엇을 할 수 있는지, 그리고 AI에 대해 저커버그는 어떤 생각을 하고 있는지 살펴 보세요. 원문은 해당 링크(<a href="https://www.facebook.com/notes/mark-zuckerberg/building-jarvis/10154361492931634" rel="nofollow" class="in_article_link">https://www.facebook.com/notes/mark-zuckerberg/building-jarvis/10154361492931634</a>)에서 확인하실 수 있습니다.</p>
<p><strong>‘자비스(Jarvis)’ 구축하기</strong></p>
<p>2016년 한 해 동안 저는 개인적인 프로젝트를 하나 진행했습니다. 바로 &lt;아이언맨&gt;에 등장하는 ‘자비스’처럼 집안일을 도와 주는 간단한 인공지능(AI)을 구축하는 일인데요.</p>
<p>프로젝트 기간 동안, AI의 놀라운 발전을 직접 경험하는 동시에 아직 갈 길이 멀다는 것 역시 깨달을 수 있었습니다.</p>
<p>‘자비스’는 스마트폰과 컴퓨터를 매개체로 사람의 말을 이해하고 조명∙온도∙가전∙음악∙보안 등 각종 집안 시설을 제어할 수 있습니다. 또한 자비스는 사람의 취향과 습관을 학습할 수 있으며 새로운 단어와 개념을 학습하고, 심지어 아이와 놀아줄 줄도 아는 똑똑한 AI입니다. 자비스 개발에는 자연어 처리, 음성 인식, 얼굴 인식, 강화 학습처럼 다양한 AI 기술과 파이썬, PHP, 오브젝티브-C 등 다양한 프로그래밍 언어가 사용됐습니다.</p>
<p>지금부터 여러분께 자비스를 소개합니다. 그리고 이 프로젝트를 진행하면서 제가 배우고 느낀 점에 대해 말씀드리겠습니다.</p>
<p><img class="aligncenter" src="https://scontent-hkg3-1.xx.fbcdn.net/v/t31.0-8/p720x720/15419743_10103347287954901_2744013366467623932_o.jpg?oh=8060e1ce7fd886f87aea7df31b749bdb&amp;oe=58E915AF" alt="" width="500" height="190"></p>
<p style="text-align: center">자비스 구축을 위해 연결된 시스템 구성</p>
<p><strong>시작은 집안을 연결하는 것부터</strong></p>
<p>집안에 있는 시스템을 서로 연결하는 것은 생각보다 복잡했습니다. 시스템들이 각기 다른 프로그래밍 언어와 프로토콜로 이뤄져 있었고, 대부분의 가전제품은 인터넷에 연결조차 돼 있지 않았기 때문입니다.</p>
<p>자비스와 같은 AI 도우미들이 미래에 보다 널리 사용되기 위해서는 더 많은 기기를 서로 연결할 수 있는 공통 API와 같은 표준이 필요하다는 것을 알 수 있었습니다.</p>
<p><strong>자연어</strong></p>
<p>다음 단계는 집안 시스템들이 사람의 말을 알아들을 수 있도록 하는 일이었습니다. 우선, 자비스와 사람이 문자로 소통할 수 있는 체계를 만들기로 했습니다. 그 다음, 사람의 목소리를 문자로 변환하고, 자비스가 저에게 하고 싶은 말을 소리로 전달할 수 있는 능력을 추가했습니다.</p>
<p>처음에는 ‘침실’, ‘전등’, ‘스위치 켜줘’와 같은 기본적인 키워드로 시작했습니다. 이 과정에서 자비스에게 ‘화장실’이나 ‘욕실’과 같은 유의어를 학습시킬 필요가 있다는 것을 자연스럽게 터득할 수 있었습니다. AI에게 맥락을 이해시키는 일의 중요성도 깨달았습니다. AI가 사람이 전하고자 하는 맥락을 정확히 이해해야 보다 어려운 열린 질문에도 능숙하게 대처할 수 있기 때문입니다.</p>
<p><strong>비전인식과 얼굴인식</strong></p>
<p>AI가 이미지와 동영상에 담긴 정보를 이해하는 과정에는 추적, 사물 인식, 얼굴 인식 등이 매우 중요합니다. 시각 정보를 이해하는 AI 시스템의 활용 가능성은 무궁무진합니다. 일례로, 아기가 낮잠에서 깬 것을 알아채고 음악을 틀어줄 수도 있고, “불 좀 켜줘”라는 명령을 듣고 사람이 어느 방에 있는지 파악해 방의 전등을 켜는 일 등을 들 수 있습니다.</p>
<p><img loading="lazy" class=" aligncenter" src="https://scontent-hkg3-1.xx.fbcdn.net/v/t31.0-8/15591179_10103347986300411_2605551985241785524_o.jpg?oh=86ff853df599067c736b7e3ac35c4b21&amp;oe=58FC8E7B" alt="" width="250" height="445"></p>
<p style="text-align: center">자비스는 현관문 앞 손님의 얼굴을 인식해 누가 방문했는지 알려줍니다.</p>
<p><strong>메신저 봇</strong></p>
<p>자비스는 컴퓨터를 기반으로 구축된 AI이지만, 시간과 장소에 대한 제약 없이 자유롭게 대화를 주고받기 위해서는 스마트폰을 활용할 필요가 있었습니다. 이를 위해 Facebook 메신저 봇을 사용했고요. Facebook 메신저 플랫폼이 제공하는 봇 프레임워크를 활용하면 별도의 앱을 구축하는 것보다 훨씬 적은 시간과 노력으로도 목적에 부합하는 메신저 봇을 개발할 수 있기 때문입니다.</p>
<p>이를 통해, 언제 어디서든 자비스와 대화를 주고받을 수 있게 됐습니다. 스마트폰을 통해 자비스 봇에게 메시지를 보내면, 메시지는 즉각 자비스 서버로 전송됩니다. 자비스 봇에게 음성 메시지를 보내는 것도 가능합니다. 음성 메시지는 서버에서 문자로 변환된 후 문자 메시지와 같은 방식으로 처리됩니다.</p>
<p>자비스를 이용하면서 놀라웠던 점은, 문자와 음성을 모두 사용할 수 있는 상황에서 문자를 선택하게 되는 경우가 생각보다 많다는 사실이었습니다. 여기에는 많은 이유가 있겠지만, 내 주변 사람들에게 불편을 끼치지 않고도 문자로 원하는 바를 전달할 수 있다는 점이 크게 작용한다고 생각합니다. 자비스로부터 메시지를 받을 때에도 텍스트로 전달받는 방식이 편했습니다. 음성에 비해 문자는 내가 원할 때 읽을 수 있다는 점에서 편리하기 때문입니다.</p>
<p><img loading="lazy" class=" aligncenter" src="https://scontent-hkg3-1.xx.fbcdn.net/v/t31.0-8/15577989_10103347985661691_4152643580570731663_o.jpg?oh=a52bb26dfbcb7e130a4e1e6f10271dda&amp;oe=58AF99C3" alt="" width="250" height="445"></p>
<p style="text-align: center">메신저 봇 덕분에 언제 어디서든 자비스에게 메시지 보내기</p>
<p><strong>음성 인식</strong></p>
<p>AI와 사람 사이의 의사소통에 있어 문자가 중요한 부분을 차지할 것이 예측되지만, 음성 역시 매우 중요한 역할을 담당하리라 생각합니다. 음성은 편리하고 신속하기 때문입니다.</p>
<p>저는 자비스가 음성을 인식할 수 있도록 전용 iOS 앱을 개발했습니다. 외출 중에도 스마트폰으로 자비스에게 말을 걸어야 하는 상황이 자주 있었기 때문이죠. 항상 음성을 인식할 준비가 돼 있는 앱 덕분에 언제나 자비스에게 말을 걸 수 있습니다. 해당 앱은 곧 안드로이드 버전으로도 개발할 계획입니다.</p>
<p>눈부신 발전에도 불구하고 AI가 음성 인식으로 사람들의 일상적인 대화를 이해하는 데는 아직 부족한 점이 많습니다. 새로이 음성 인식을 적용할 수 있는 분야도 무궁무진합니다. AI와 음성 인식 기술은 꾸준히 앞을 향해 나아가고 있으며, 몇 년 후에는 더욱 발전된 모습을 보여주리라 기대합니다.</p>
<p><img loading="lazy" class=" aligncenter" src="https://scontent-hkg3-1.xx.fbcdn.net/v/t31.0-8/p720x720/15578281_10103347313693321_3998052187899228050_o.jpg?oh=9f0259c686aa93af7a073b1368b672e9&amp;oe=58F9ECE9" alt="" width="250" height="445"></p>
<p style="text-align: center">자비스를 위한 iOS 앱 음성 인식 기능</p>
<p><strong>다음 단계는?</strong></p>
<p>올해의 도전은 여기서 마칩니다만, 앞으로도 매일같이 자비스를 사용하고 꾸준히 발전시킬 계획입니다.</p>
<p>단기 목표로는 안드로이드 앱 개발을 꼽을 수 있겠고, 이와 더불어 더 많은 방에 자비스 음성 단말기를 설치할 계획입니다. 아울러 더 많은 가전기기를 서로 연결하는 것도 빼놓을 수 없겠죠. 장기적으로는 자비스에게 자가 학습 능력을 가질 수 있도록 개발을 진행하고자 합니다. 물론, 자비스를 세상의 많은 사람들에게 선보일 방법을 찾는 것 역시 중요하고 재미있는 과제가 될 것입니다.</p>
<p><strong>결론</strong></p>
<p>이번 프로젝트는 무척이나 흥미로운 지적 도전 그 자체였습니다. 미래를 위한 AI 도구를 직접 구축해 보는 직접적인 경험을 할 수 있는 계기이기도 했고요.</p>
<p>이번 도전을 지켜보고 함께해 주신 여러분께 감사의 인사를 전합니다. 몇 주 안으로 2017년을 위한 제 새로운 도전에 대해 말씀드릴 계획이니 응원을 부탁드립니다.</p>
<p>&nbsp;</p>
<p>아래는 저커버그 아내 입장에서 만나본 자비스 영상입니다. 부록 정도 되겠네요.</p>
<div class="fb-video fb_iframe_widget fb_iframe_widget_fluid_desktop" data-allowfullscreen="true" data-href="https://www.facebook.com/zuck/videos/10103351403412491/" style="width: 100%;" fb-xfbml-state="rendered" fb-iframe-plugin-query="allowfullscreen=true&amp;app_id=249643311490&amp;container_width=510&amp;href=https%3A%2F%2Fwww.facebook.com%2Fzuck%2Fvideos%2F10103351403412491%2F&amp;locale=ko_KR&amp;sdk=joey"><span style="vertical-align: bottom; width: 510px; height: 261px;"><iframe name="f536ff8aeb0994" width="1000px" height="1000px" data-testid="fb:video Facebook Social Plugin" title="fb:video Facebook Social Plugin" frameborder="0" allowtransparency="true" allowfullscreen="true" scrolling="no" allow="encrypted-media" src="https://www.facebook.com/v2.3/plugins/video.php?allowfullscreen=true&amp;app_id=249643311490&amp;channel=https%3A%2F%2Fstaticxx.facebook.com%2Fx%2Fconnect%2Fxd_arbiter%2F%3Fversion%3D46%23cb%3Df3248f85e3318c%26domain%3Dabout.fb.com%26is_canvas%3Dfalse%26origin%3Dhttps%253A%252F%252Fabout.fb.com%252Ff33d182c3c2ea2%26relation%3Dparent.parent&amp;container_width=510&amp;href=https%3A%2F%2Fwww.facebook.com%2Fzuck%2Fvideos%2F10103351403412491%2F&amp;locale=ko_KR&amp;sdk=joey" style="border: none; visibility: visible; width: 510px; height: 261px;" class=""></iframe></span></div>
		</div>
<div id="related_posts" class="uk-container related-posts" data-gtm-vis-recent-on-screen-12696809_202="736485" data-gtm-vis-first-on-screen-12696809_202="736486" data-gtm-vis-total-visible-time-12696809_202="300" data-gtm-vis-recent-on-screen-12696809_238="736486" data-gtm-vis-first-on-screen-12696809_238="736486" data-gtm-vis-total-visible-time-12696809_238="300" data-gtm-vis-recent-on-screen-12696809_303="736486" data-gtm-vis-first-on-screen-12696809_303="736486" data-gtm-vis-total-visible-time-12696809_303="300" data-gtm-vis-has-fired-12696809_202="1" data-gtm-vis-has-fired-12696809_238="1" data-gtm-vis-has-fired-12696809_303="1">
		<h2 class="related-posts-title section-title ui-subheading1">관련 뉴스</h2>
		<div class="uk-grid uk-flex uk-flex-center news-cards archive-articles-container">
				
			<article id="post-22922" class="uk-flex uk-width-1-1@s uk-card uk-animation-fade news-card post-22922 post type-post status-publish format-standard hentry category-facebook-app category-instagram category-messenger category-oculus category-meta">
		    <div class="uk-width-3-5 article-excerpt">
		        <header class="entry-header">
					<div class="news-label label-line label-meta">
					Meta					</div>
					<h3 class="entry-title uk-margin-remove-top ui-heading2"><a href="https://about.fb.com/ko/news/2023/04/2023%eb%85%84-1%eb%b6%84%ea%b8%b0-meta-%ec%8b%a4%ec%a0%81-%eb%b0%9c%ed%91%9c-%ec%a3%bc%ec%9a%94-%eb%82%b4%ec%9a%a9/" rel="bookmark" class="in_article_link related_news_article_link">2023년 1분기 Meta 실적 발표 주요 내용</a></h3>					<div class="article-excerpt-body">
						Meta의 2023년 1분기 실적이 발표되었습니다.					</div>
											<div class="entry-meta">
							<span class="posted-on"><time class="entry-date published" datetime="2023-04-28T10:36:06+09:00">2023년 4월 28일</time><time class="updated" datetime="2023-04-28T10:42:31+09:00">2023년 4월 28일</time></span>						</div>				</header>
		    </div>
		    <div class="uk-width-2-5 uk-padding-remove-vertical article-featured-thumbnail">
		        	<div class="featured-image-container aspect-image-container">
																<div class="aspect-wrap bg-aspect-wrap">
				<div class="aspect-spacer bg-aspect-spacer" style="padding-bottom: 75%;"></div>
				<span class="aspect bg-aspect" style="background-image: url(https://about.fb.com/ko/wp-content/uploads/sites/16/2022/10/메타-썸네일.jpg?fit=960%2C720);"></span>
			</div>
																					</div>
					
		    </div>
			</article>


			</div>
</div>



<h3 class="heading">GPT-4 발표한 오픈AI __'샘 알트만'__, "AI가 사회를 재구성할 것이며 위험을 인정합니다, 이것이 조금 두렵습니다"</h3>
<h4 class="subheading">AI가 일자리를 대체할 것인가? 에 대해서 알트만은 이것이 가까운 장래에 일부 일자리를 대체할 가능성이 있으며 얼마나 빨리 일어날 수 있는지 걱정하고 있다고 밝혔다.</h4>
<div style="text-align:center">
<figure class="photo-layout image photo_41566 float-center bigsize" data-idxno="41566" data-type="photo" style="display:inline-block; max-width:960px"><img alt="오픈AI CEO 샘 알트만(사진:ABC방송 캡처)" src="https://cdn.aitimes.kr/news/photo/202303/27595_41566_124.jpg">
<figcaption>오픈AI CEO 샘 알트만(사진:ABC방송 캡처)</figcaption>
</figure></div>
<p>대화형 생성 인공지능(Generative AI) 챗GPT(ChatGPT)의 오픈AI CEO 샘 알트만(Sam Altman)는 인공지능 기술이 우리가 알고 있는 사회를 재구성할 것이라며, 실제 위험이 따르지만 우리의 삶을 획기적으로 개선하기 위해 "인류가 지금까지 개발한 가장 위대한 기술"이 될 수도 있다고 믿는다고 17일(현지시간) ABC방송 인터뷰를 통해 밝혔다.</p>
<p>이날 알트만은 ABC 뉴스의 수석 비즈니스, 기술 및 경제 특파원인 레베카 자비스(Rebecca Jarvis)와 독점 인터뷰를 통해 대형 AI 언어 모델이자 사전 학습된 생성형 트랜스포머 모델의 최신 버전인 GPT-4의 출시에 대한 소회(所懷)를 밝혔다</p>
<p>인터뷰에서 알트만은 OpenAI가 챗GPT의 출시에 가능한 한 규제 기관과 사회 모두가 관여해야 한다고 강조했다. 또한 이 기술에 대한 피드백은 기술이 인류에게 미칠 수 있는 잠재적인 부정적인 결과를 억제하는 데 도움이 될 것이라고 주장했다. 그는 정부 관리들과 정기적으로 접촉하고 있다고 덧붙였다.</p>
<p>불과 몇 달 전에 출시된 이 제품은 이미 역사상 가장 빠르게 성장했으며, 이 앱은 불과 3개월 만에 월 활성 사용자 수 1억 명을 돌파했다. 이에 비해 UBS 연구에 따르면 틱톡(TikTok)은 이 수준에 도달하는 데 9개월이 걸렸고 인스타그램(Instagram)은 거의 3년이 걸렸다 .</p>
<p>알트만에 따르면 "완벽하지는 않지만" GPT-4는 미국 변호사 시험(UBE, Uniform Bar Exam)에서 90번째 백분위수를 기록했다. 또한 SAT 수학 시험에서 만점에 가까운 점수를 얻었으며 이제 대부분의 프로그래밍 언어로 컴퓨터 코드를 능숙하게 작성할 수 있다.</p>
<p>또 알트만은 "GPT-4는 AI가 일반적으로 인간보다 더 똑똑한 AI 시스템으로 설명될 수 있는 강력한 임계값을 넘을 때 최종적으로 인공일반지능(AGI, Artificial General Intelligence)을 구축하려는 OpenAI의 목표를 향해 내딘 한 걸음에 불과하다"고 말했다.</p>
<p>아울러 알트만은 이 모델의 성공에도 불구하고 밤잠을 설치게 만들 정도로 AI의 위험한 구현 가능성을 밝히며 그는 "이러한 모델이 대규모 허위 정보에 사용될 수 있다는 점과 컴퓨터 코드를 더 잘 작성하고 있으므로 사이버 공격 등 악의적으로 사용될 수 있다"며 우려했다.</p>
<p>이어 그는 "우리가 설정한 안전 한계를 설정하지 않는 다른 사람들이 있을 것"이라며, "어떤 이들은 AI 사용에 있어서 안전장치 등 제한을 두지 않을 수도 있다며 어떻게 통제할지 생각해내야 하는데, 그럴 수 있는 시간은 제한돼 있다"고 했다.</p>
<p>그는 블라디미르 푸틴 대통령이 2017년 개학 첫날 러시아 학생들에게 AI 경주를 주도하는 사람이 "세계를 지배할 것"이라고 말한 것을 인용하며, 그 말에 대해 "오싹한 진술이다"라고 말하며, "대신 내가 희망하는 것은 우리 모두가 AI를 우리의 일상생활과 경제에 통합하고 인간 의지를 증폭시키는 다양한 방식으로 사용할 수 있는 점점 더 강력한 시스템을 지속적으로 개발하는 것입니다"라고 밝혔다.</p>
<p>이어 알트만은 "제가 사람들에게 가장 주의를 기울이는 것은 '환각 문제'입니다."라며, "모델은 마치 완전히 꾸며낸 사실인 것처럼 자신 있게 말하게 됩니다"라며, "이전 모델은 부분적으로 암기보다는 연역적 추론을 사용하기 때문에 이 문제가 있습니다. GPT-3.5 모델 대비 GPT-4로 본 가장 큰 차이점 중 하나는 더 나은 추론 능력입니다"라고 말했다.</p>
<p>알트만은 이에 대해 "우리가 만드는 모델을 생각하는 올바른 방법은 사실 데이터베이스가 아니라 추론 엔진입니다"라며, "그들은 또한 사실 데이터베이스의 역할을 할 수 있지만 그것이 그들에게 특별한 점은 아닙니다. 우리가 원하는 것은 기억하는 것이 아니라 추론하는 능력에 더 가까운 것입니다"라고 강조하며, "결국 인터넷과 자체 연역적 추론을 사용하여 사실과 허구를 구분할 수 있게 될 것입니다“라고 덧붙였다.</p>
<p>OpenAI에 따르면 GPT-4는 GPT-3.5보다 허용되지 않는 콘텐츠에 대한 요청에 응답할 가능성이 82% 적고 사실에 입각한 응답을 할 가능성이 40% 더 높다고 한다. 그러나 알트만은 정확한 정보의 주요 소스로 시스템에 의존하는 것은 "사용해서는 안 되는 것"이며 사용자가 프로그램 결과를 다시 확인하도록 권장한다고 밝혔다.</p>
<p>또한 AI가 일자리를 대체할 것인가? 에 대해서는 알트만은 이것이 가까운 장래에 일부 일자리를 대체할 가능성이 있으며 얼마나 빨리 일어날 수 있는지 걱정하고 있다고 밝혔다.</p>
<p>알트만은 "몇 세대에 걸쳐 인류는 주요 기술 변화에 훌륭하게 적응할 수 있음을 입증했습니다. 하지만 이런 일이 한 자릿수 년 안에 일어난다면, 이러한 변화 중 일부는 제가 가장 걱정하는 부분입니다."라며, 그러나 그는 사람들이 챗GPT를 어떤 일이나 직업에 대체품이 아닌 도구로 작용할 것이라고 말했다.</p>
<p>그는 이에 대해 "인간의 창의성은 무한합니다. 우리는 이를 통해 새로운 직업과 새로운 할 일을 찾을 것입니다" 라고 덧붙였다. (더 자세한 이날 인터뷰 내용을 아래 영상을 참고하면 된다.)</p>
<div class="simplebox" style="text-align:center;">
<div class="simplebox-content video_10247" data-idxno="10247" data-type="video"><iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="" frameborder="0" height="480" src="https://www.youtube.com/embed/540vzMlf-54" title="YouTube video player" width="854"></iframe></div>
</div>
<p>한편,&nbsp;오픈AI가 14일(현지시간) GPT-4를 전격 공개했다. 고급 추론(reasoning) 기능으로 폭넓은 일반 지식과 문제 해결 능력 덕분에 어려운 문제를 더 정확하게 풀 수 있다. 이를 통해 지난 몇 달 동안 폭발적인 인기를 끌었던 챗GPT(ChatGPT)는 GPT-3.5와 상호작용하는 방식이었으나 이제는 GPT-4와 상호작용하는 방식이 된 것이다.</p>
<p>GPT-4는 월 20달러를 지불하는 유료 서비스인 챗GPT플러스(ChatGPT Plus)에서 사용할 수 있으며 개발자를 위한 API와 무료 데모도 제공됐다.</p>
<p>이날 오픈AI는 GPT-4와 함께 AI 모델의 성능을 평가하기 위한 소프트웨어 프레임워크 에벌즈(Evals)를 오픈소스로 공개했다. 이 도구를 통해 누구나 모델의 문제와 단점을 제시하여 모델을 개선할 수 있다.</p>
<p>오픈AI는 GPT-4는 챗GPT의 약 8배인 최대 25,000단어까지 처리할 수 있으며, 안전과 정치적으로 편향되거나 극단적으로 공격적이거나 때에 따라 서로 다른 방식의 결과, 거짓말 등의 최근 이슈를 인정하고 이를 보완하기 위해 6개월을 보냈고 그동안의 피드백에 대해 학습(수많은 악성 프롬프트)했다고 밝혔다.</p>
<p>그러나, 이날 오픈AI 샘 알트만(Sam Altman) CEO는 트위터를 통해 “가장 성능이 뛰어나고 잘 정돈된 모델이지만 이 역시 여전히 잘못된 정보를 공유하는 경향이 있을 수 있다"고 경고했다.(GPT-4 논문 Technical Report&nbsp;<a href="https://cdn.openai.com/papers/gpt-4.pdf" target="_blank"><span style="color:#ffffff;"><span style="background-color:#8e44ad;">다운</span></span></a>)</p>
<p>현재, 인공지능 세계는 영어 사용자가 지배하고 있다. 데이터에서 테스트, 연구 논문에 이르기까지 거의 모든 것이 영어로 되어 있다. 그러나 물론 대규모 언어 모델(LLM)의 기능은 모든 서면 언어에 적용 가능하며, 해당 언어에서 사용할 수 있어야 한다.</p>
<div style="text-align:center">
<figure class="photo-layout image photo_41564 float-center bigsize" data-idxno="41564" data-type="photo" style="display:inline-block; max-width:1038px"><img alt="여러 언어에 걸친 MMLU의 GPT-4 3-샷 정확도(Azure Translate를 사용하여 57개 주제에 걸친 14,000개의 객관식 문제 모음인 MMLU 벤치마크를 다양한 언어로 번역. 테스트한 26개 언어 중 24개 언어에서 GPT-4는 라트비아어, 웨일스어, 스와힐리어와 같은 리소스가 적은 언어를 포함하여 GPT-3.5 및 기타 LLM(Chinchilla, PaLM)의 영어 성능을 능가" src="https://cdn.aitimes.kr/news/photo/202303/27595_41564_2253.jpg">
<figcaption>여러 언어에 걸친 MMLU의 GPT-4 3-샷 정확도(Azure Translate를 사용하여 57개 주제에 걸친 14,000개의 객관식 문제 모음인 MMLU 벤치마크를 다양한 언어로 번역. 테스트한 26개 언어 중 24개 언어에서 GPT-4는 라트비아어, 웨일스어, 스와힐리어와 같은 리소스가 적은 언어를 포함하여 GPT-3.5 및 기타 LLM(Chinchilla, PaLM)의 영어 성능을 능가</figcaption>
</figure>
</div>
<p>이에 GPT-4의 다국어 기능은 한국어부터 이탈리아어, 우크라이나어에 이르기까지 26개 언어에 걸쳐 수천 개의 객관식 질문에 높은 정확도로 답변할 수 있음을 보여줌으로써 AI 민주화를 위한 한 걸음을 내디뎠다.</p>
<p>특히,&nbsp;GPT-3.5에서 영어 인식 성능이 70.1%를 기록했다. 반면 새로운 GPT-4에서는 한국어 인식 성능이 놀랍게도 77%를 기록했다. 이전의 전 세계 AI 이슈를 뿌리던 챗GPT 영어 인식 성능보다&nbsp;GPT-4의 한국어 인식 성능이 높다는 것은 그동안 '한국형 특화'를 내세웠던 AI 기업들은 새겨야 할 시점이다.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
<p>또한 그 중에서도 가장 눈에 띄는 변화는 '멀티모달(Multimodal)'로 이전의 챗GPT 및 GPT-3는 텍스트로 제한되었지만 GPT-4는 이미지를 보고 이해하고 설명하고 요청한 사항을 처리한다. 예를 들어, 재료 사진에서 레시피 제안을 제공하고 캡션 및 설명을 작성할 수 있으며, 더 중요한 것은 라벨을 번역하고, 지도를 읽는 등 다양한 분야에서 이해도가 그 이상이라고 한다. (자세한 내용은 본지 15일 보도 <a href="https://cms.aitimes.kr/news/articleView.html?idxno=27571" target="_blank"><span style="color:#ffffff;"><span style="background-color:#e74c3c;">참조</span></span></a>)</p>


