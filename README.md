    def encrypt(text, shift): #构建加密函数
        result = ""
        for c in text: #循环遍历输入
            if c.isupper():
                result += chr((ord(c) - ord('A') + shift) % 26 + ord('A'))
            elif c.islower():
                result += chr((ord(c) - ord('a') + shift) % 26 + ord('a'))
            else:
                result += c
        return result

    def decrypt(text, shift): #构建解密函数
        return encrypt(text, -shift) 

    def main():
        print("凯撒密码加解密工具")
        choice = input("请选择 1.加密 2.解密：") #选择加密解密
        text = input("请输入内容：") #输入内容
        shift = int(input("请输入偏移量（1-25）：")) #选择偏移量

        if choice == "1":
            print("加密结果：", encrypt(text, shift))
        elif choice == "2":
            print("解密结果：", decrypt(text, shift))
        else:
            print("输入错误")
        #不同结果输出
    main()#执行函数

https://github.com/user-attachments/assets/34f24271-009d-4d36-8a31-4f02decbd934

![微信图片_20260316232136_108_20](https://github.com/user-attachments/assets/26031400-2882-481c-8712-cda5319e796f)
