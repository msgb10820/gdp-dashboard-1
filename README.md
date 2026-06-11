import streamlit as st

# 1. 앱 인터페이스 및 제목 설정
st.set_page_config(page_title="나만의 신발 제작소", page_icon="👟")
st.title("👟 나만의 신발 제작소")
st.write("원하는 옵션을 선택하여 나만의 신발을 완성하세요!")

st.divider()

# 2. 신발 색상 선택 (원본 코드의 로직 반영)
color_list = ["선택하세요", "검정", "하양", "노랑"]
color = st.selectbox("신발색(검정, 하양, 노랑):", color_list)

# 3. 장식 선택 (원본 코드의 로직 반영)
deco_list = ["선택하세요", "줄무늬", "점박이", "하트무늬"]
deco = st.selectbox("장식(줄무늬, 점박이, 하트무늬):", deco_list)

# 4. 신발 종류 선택 (원본 코드의 로직 반영)
kind_list = ["선택하세요", "운동화", "구두", "슬리퍼"]
kind = st.selectbox("신발종류(운동화, 구두, 슬리퍼):", kind_list)

st.divider()

# 5. 모든 항목이 선택되었는지 확인 (원본의 while문/if문 조건)
if color != "선택하세요" and deco != "선택하세요" and kind != "선택하세요":
    # 완성 버튼
    if st.button("신발 완성하기 ✨"):
        st.balloons() # 축하 애니메이션
        st.success("🎉 나만의 신발이 완성되었습니다!")
        
        # 최종 결과 출력 (원본의 print 내용과 동일)
        st.subheader("[ 제작 주문서 ]")
        st.info(f"🎨 신발색: {color}")
        st.info(f"✨ 장식: {deco}")
        st.info(f"👟 신발종류: {kind}")
else:
    # 선택이 덜 되었을 때 안내 (원본의 '다시 입력해주세요' 역할)
    st.warning("모든 옵션을 선택해주셔야 신발을 제작할 수 있습니다.")