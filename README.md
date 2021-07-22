# rsa
pem生成、加密、解密

# 加密解密用法示例

```
func main() {
	//RSA加密
	data, err := RsaEncrypt([]byte("12345"), "publicKey.pem")
	if err != nil {
		panic(err)
	}
	fmt.Println("RSA加密", string(data))

	//RSA解密
	origData, err := RsaDecrypt(data, "privateKey.pem")
	if err != nil {
		panic(err)
	}
	fmt.Println("RSA解密", string(origData))
}
```
