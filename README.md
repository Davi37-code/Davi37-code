from xxlimited import foo
from selenium import webdriver 
from selenium.webdriver.common.by import By 
from selenium.webdriver.common.keys import Keys 
from selenium.webdriver.chrome.service import Service 
from webdriver_manager.chrome import ChromeDriverManager 
import time 
import schedule 

# 1. Configurar o Selenium para usar o ChromeDriver gerenciado automaticamente 
browser = webdriver.Chrome(service=Service(ChromeDriverManager().install())) 

# 2. Abrir o WhatsApp Web 
browser.get("https://web.whatsapp.com/") 

# 3. Aguardar o usuário escanear o QR Code manualmente 
print("Por favor, escaneie o QR Code para fazer login no WhatsApp Web.") 
time.sleep(15) # Pausa de 15 segundos para você escanear o código com o celular 

def enviar_mensagem():  
    from:
	# 4. Localizar o grupo pelo nome (coloque o nome exato do grupo entre as aspas) 
	nome_do_grupo = "🇧🇷 Brasileiros na Espanha 🇪🇸"		 
	grupo = browser.find_element(By.XPATH, f"/[@title='{nome_do_grupo}']")		 
	grupo.click()		 

	# 5. Localizar a caixa de texto de mensagem e enviar a mensagem 
	mensagem = """*AINDA BUSCANDO VAGAS?*😓		 
Paga por um Europass genérico ❌			 
Compete com muitos na Europa ❌			 
Infojobs e Linkedin te descartam❌			 

*CONSULTORIA ESPECIALIZADA* 
*VAGAS EUROPA*(🇪🇸🇵🇹🇫🇷🇬🇧🇩🇪) 
📃*OTIMIZAMOS CURRÍCULOS* 
📃 CV longo. É 👵🏻, experiência 0 ❌ 
Estratégico e direcionado a perfil ✅ 
RHs pedindo para te entrevistar ✅ 

🇪🇺*EMPRESAS EUROPEIAS* 🇪🇺 
Preferem os nativos a você ❌ 
Você com um salário decente ✅ 
Voltando a estudar e crescer ✅ 

⏱️*EFICIENCIA DO TEMPO*⏱️ 
Cadastra o CV em muitos sites ❌ 
Enviamos para os RHs certos ✅ 

👨🏻‍💻*HEADHUNTERS & PODER*👨🏻‍💻 
Eles olham 200 currículos ao dia ❌ 
Quem te escolhe tem influência ✅ 
O seu CV chegando a decisores ✅ 

🔍*AUMENTO DE RELEVANCIA*🔍 
Trabalha com qualquer coisa ❌ 
Trabalhe no seu nicho e cidade ✅ 
Seu idioma, sua especialização ✅ 

🏆*COMO SER CONTRATADO*🏆 
Não passa, não dão feedback ❌ 
Simulação de entrevista 🇪🇸& 🇬🇧 ✅ 
Como ser contratado(a) na hora ✅ 

📊*LINKEDIN TRENDS & SEO*📊 
Não sabe usar. Não recomenda ❌ 
Seu perfil otimizado nas buscas ✅ 
Como ser encontrado e indicado ✅ 

✈️*QUERO ME DESTACAR*✈️ 
https://wa.me/message/5NDCOGD6WOA4K1""" 

	caixa_de_texto = browser.find_element(By.XPATH, "//div[@contenteditable='true']") 
	caixa_de_texto.send_keys(mensagem + Keys.ENTER) 

	print(f"Mensagem enviada com sucesso para o grupo '{nome_do_grupo}'!") 
except Exception as e: 
	print(f"Erro ao enviar mensagem: {e}") 

# 6. Agendar o envio para horários específicos (manhã, tarde e noite) 
schedule.every().day.at("08:00").do(enviar_mensagem) # Enviar às 8h00 
schedule.every().day.at("12:00").do(enviar_mensagem) # Enviar às 12h00 
schedule.every().day.at("18:00").do(enviar_mensagem) # Enviar às 18h00 

# 7. Loop principal para manter o agendamento ativo 
while True: 
	schedule.run_pending() 
	time.sleep(1)
```- 👋 Hi, I’m @Davi37-code
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Davi37-code/Davi37-code is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
