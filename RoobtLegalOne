from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support.ui import Select
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.support.ui import WebDriverWait
import time 
from selenium.webdriver.common.action_chains import ActionChains
from openpyxl import workbook, load_workbook
import pandas as pd 
from selenium.webdriver.support import expected_conditions as EC
from datetime import datetime

planilha = load_workbook('A RECEBER 1.xlsx')
plan = planilha.active
plan = planilha.worksheets[0]

planilha = load_workbook('TRANSFERENCIA 1.xlsx')
plan = planilha.active
plan = planilha.worksheets[0]

chrome_options = Options()
chrome_options.add_argument("--headless")   

def login(navejgar, user, password):
    try:
        WebDriverWait(navejgar, 5).until(EC.element_to_be_clickable((By.ID, 'Username')))
        inpulogin = navejgar.find_element(By.ID, 'Username')
        inpulogin.clear()
        inpulogin.send_keys(user)

        inputpass = navejgar.find_element(By.ID, "Password")
        inputpass.clear()
        inputpass.send_keys(password)
        time.sleep(5)

        botton = navejgar.find_element(By.ID, 'SignIn')
        botton.click()
        time.sleep(2)
    except:
        print("Erro ao fazer o login")

def preencher_campos_areceber(navejgar, plan):
    try:
        # Preencher proprietário
        proprietario = WebDriverWait(navejgar, 10).until(EC.element_to_be_clickable((By.ID, 'ProprietarioText')))
        proprietario.clear()
        proprietario.send_keys(plan['A2'].value + Keys.ENTER)
    except Exception as e:
        print(f"Erro ao inserir as informações: {e}")       

def main():
    navejgar = webdriver.Chrome()
    navejgar.get("https://arantesarimura.novajus.com.br/financeiro/obrigacoesareceber/create?returnUrl=%2Ffinanceiro%2Fobrigacoes%2FSearch")

    user = 'Login'
    password = 'Senha'

    try: 
        print('fazendo o login')
        login(navejgar, user,  password)
        time.sleep(5)
        preencher_campos_areceber(navejgar, plan)
    finally:
        navejgar.quit()

if __name__ == "__main__":
    main()         
