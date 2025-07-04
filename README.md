from PIL import Image

import requests
import streamlit as st
from streamlit_lottie import st_lottie




st.set_page_config(page_title="HELLO WORLD" , page_icon="ChatGPT Image Mar 31, 2025, 04_09_22 PM.png",layout="wide")
#-----ANIMATION-----

def load_lottie(url):
    r = requests.get(url)
    if r.status_code != 200:
        return None
    return r.json()
lottie_coding = load_lottie("https://lottie.host/239e4c5b-86f5-4ddb-840f-b4c7585e572a/oiad7aK7Tl.json")
img = Image.open("ChatGPT Image Mar 31, 2025, 04_09_22 PM.png")
# HEADER PART # ---
with st.container():
    st.title("A student learning python")
    st.header("HI I AM MANAV :smiley:")
    st.write("nkfirhuhfohfiegfgseigiu")
    st.write("[to learn more >](https://youtube.com)")

with st.container():
    st.write("---")
    left_column , right_column  =st.columns(2)
    with left_column :
        st.header("WHT DO I DO ")
    with right_column:
        st_lottie(lottie_coding, height = 300 , key="coding")

with st.container():
    st.write("---")
    image_column , text_coloumn = st.columns((1000,3000))
    with image_column:
        st.image(img)
    with text_coloumn:
        st.markdown("<h1 style='font-size: 100px;'>SO HERE WE GO AGAIN </h1>", unsafe_allow_html=True)
