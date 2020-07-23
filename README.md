# python
python
### 'read()' command is being used to open txt files i think.
### WE SHOULD FIRST IMPORT DOCX


f = open(r"C:\Users\cenke\PycharmProjects\PortalV2\portalinfo.txt")
print(f.readline())
userName = "cenkerozkan"
userPassword = "Cenker3298"
name = input("Lütfen kullanıcı adınızı giriniz: ")
password = input("Lütfen şifrenizi giriniz: ")
if (name == userName and password == userPassword):
        print("Üniversite adı --- 2018 Sıralama --- 2019 Sıralama --- 2020 Sıralama")
        print("Giriş başarılı")
        print("Üniversiteleri (g)enel olarak mı görmek istersiniz yoksa (s)pesifik olarak görmek istediğiniz bir okul mu var ?")
        choice = input("")
        if choice == "g":
            privateCollages = ("1 - Koç Üniversitesi(%100)", "2 - Bilkent Üniversitesi(%100)", "3 - Koç Üniversitesi(%50)"
                           , "4 - Koç Üniversitesi(%25)", "5 - Bilkent Üniversitesi(%50)",
                           "6 - TOBB Ekonomi Üniversitesi(%100)"
                           , "7 - Özyeğin Üniversitesi(%100)", "8 - TOBB Ekonomi Üniversitesi(%75)")
            privateCollagesRank2018 = ("244", "1208", "2880", "4214", "4892", "5031", "6004", "7354")
            privateCollagesRank2019 = ("208", "917", "3111", "9970", "4501", "4250", "4135", "5552")
            privateCollagesRank2020 = ("281", "722", "3532", "9011", "3756", "3540", "2983", "5074")

            stateCollages = (
            "1 - Boğaziçi Üniversitesi", "2 - Orta Doğu Teknik Üniversitesi", "3 - İstanbul Teknik Üniversitesi"
            , "4 - Galatasaray Üniversitesi", "5 - Abdullah Gül Üniversitesi", "6 - Yıldız Teknik Üniversitesi"
            , "7 - Hacettepe Üniversitesi", "8 - Marmara Üniversitesi", "9 - İzmir Yüksek Teknoloji Enstitüsü"
            )
            print("(D)evlet okullarına mı bakma istersiniz yoksa (Ö)zel okullara mı ?")
            type = input("")


            if (type == "D"):
                state = open(r"C:\Users\cenke\PycharmProjects\PortalV2\stateunigeneral.txt")
                print(state.read())
            elif type == "Ö":
                for (punis, yp18, yp19, yp20) in zip(privateCollages, privateCollagesRank2018, privateCollagesRank2019,
                                                     privateCollagesRank2020):
                    print(punis, "--", yp18, "--", yp19, "--", yp20)
        elif (choice == "s"):
            BilkentUni = ("Bilkent Üniversitesi\t1208\t917\t\t722\t\t%100\nBilkent Üniversitesi\t4892\t4501\t3756\t%50")

            Kuni = ("Koç Üniversitesi\t244\t\t208\t\t281\t\t%100\nKoç Üniversitesi\t2880\t3111\t3532\t%50\nKoç Üniversitesi\t4214\t9970\t9001\t%25")

            OzyeginUni = ("Özyeğin Üniversitesi\t6004\t4135\t2983\t%100")

            TOBBuni = ("TOBB Üniversitesi\t5031\t4250\t3540\t%100\nTOBB Üniversitesi\t7354\t5552\t5074\t%75")

            BogaziciUni = ("Boğaziçi Üniversitesi\t734\t623\t429")

            ODTU = ("Orta Doğu Teknik Üniversitesi\t2726\t2176\t1488")



            print("Hangi Üniversiteye bakmak istiyorsunuz ?")
            uniName = str(input())

            if(uniName == "bilkent"or uniName=="Bilkent" or uniName == "Bilkent Üniversitesi" or uniName=="bilkent üniversitesi"):
                print(BilkentUni)
            elif(uniName == "koç" or uniName=="Koç" or uniName=="Koç Üniversitesi" or uniName == "koç üniversitesi"):
                print(Kuni)
            elif(uniName == "öz" or uniName == "özyeğin" or uniName == "Özyeğin"):
                print(OzyeginUni)
            elif(uniName == "Tob" or uniName == "Top" or uniName == "TOBB" or uniName == "TOBB üni" or uniName == "tobb" or uniName == "top"):
                print(TOBBuni)
            elif(uniName == "odtü" or uniName == "Orta doğu teknik" or uniName == "Odtü" or uniName == "ODTÜ" or uniName == "Orta doğu teknik üniversitesi"):
                print(ODTU)

                print("Unkown process")
elif (name != userName or password != userPassword):
    print("Kullanıcı adı ya da şifresi yanlış")
    print('Kayıt olmak ister misiniz?')
    cevap = input("")
elif (cevap == "Evet" or cevap == "evt" or cevap == "e" or cevap == "E" or cevap == "evet"):
    print("Yeni kullanıcı adı")
    newUsername = input("")
    print("Yeni kullanıcı şifresi")
    newUserpassword = input("")
    userName = userName + newUsername
    userPassword = userPassword + newUserpassword
    print("Kayıt başarılı")
