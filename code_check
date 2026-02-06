import google.generativeai as genai
import streamlit as st

# إعداد المفتاح
genai.configure(api_key=st.secrets["GEMINI_API_KEY"])

st.title("🔍 فحص الموديلات")

try:
    st.write("جاري الاتصال بجوجل لجلب القائمة...")
    # هذا الكود حيجيب كل الموديلات المتاحة لحسابك
    for m in genai.list_models():
        if 'generateContent' in m.supported_generation_methods:
            st.code(m.name) # حيطبع الاسم زي models/gemini-1.5-flash
except Exception as e:
    st.error(f"مشكلة في الاتصال: {e}")
