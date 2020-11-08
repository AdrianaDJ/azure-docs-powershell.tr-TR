---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105996"
---
# New-AzureRemoteAppCollection

## SYNOPSIS
Azure RemoteApp koleksiyonu oluşturur.

## INDEKI

### Tümparametersets (varsayılan)
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AzureVNet
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Yeni-AzureRemoteAppCollection** cmdlet 'ı bir Azure RemoteApp koleksiyonu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: koleksiyon oluşturma
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

Bu komut, bir Azure RemoteApp koleksiyonu oluşturur.

### Örnek 2: kimlik bilgilerini kullanarak koleksiyon oluşturma
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

Bu komut, **Get-Credential** cmdlet 'inin kimlik bilgilerini kullanarak bir Azure RemoteApp koleksiyonu oluşturur.

## PARAMETRELERINE

### -CollectionName
Azure RemoteApp koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Azure RemoteApp sunucularına etki alanınıza katılma izni olan bir hizmet hesabının kimlik bilgilerini belirtir.
**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Customrdpözelliği
Sürücü yeniden yönlendirmeyi ve diğer ayarları yapılandırmak için kullanılabilecek özel uzak masaüstü Protocal (RDP) özelliklerini belirtir.
Ayrıntılar için [Windows Server 'Daki Uzak Masaüstü Hizmetleri 'Ndeki RDP ayarlarına](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) bakın `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Açıklama
Nesne için kısa bir açıklama belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsServers
DNS sunucularının IPv4 adreslerinin virgülle ayrılmış listesini belirtir.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Etki alanı
RD Oturumu Ana Bilgisayarı sunucularına katılacak Active Directory etki alanı Hizmetleri etki alanının adını belirtir.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GörüntüAdı
Azure RemoteApp şablonu görüntüsünün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Koleksiyonun Azure bölgesini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrganizationalUnit
RD Oturumu Ana Bilgisayarı sunucularına katılacak kuruluş biriminin (OU) adını belirtir; Örneğin, OU = msiz, DC = etkialanım, DC = ParentDomain, DC = com.
OU ve DC gibi öznitelikler büyük harf olmalıdır.
Koleksiyon oluşturulduktan sonra OU değiştirilemez.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Azure RemoteApp koleksiyonu için kullanım sınırlarını tanımlayabileceğiniz planı belirtir.
Planları görmek için **Get-AzureRemoteAppPlan** 'ı kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Koleksiyonun kaynak türünü belirtir.
Bu parametre için kabul edilebilir değerler: uygulama veya masaüstü.

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Sanal ağda, Azure RemoteApp koleksiyonunu oluşturmak için kullanılacak alt ağın adını belirtir.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vağ adı
Azure RemoteApp sanal ağının adını belirtir.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppPlan](./Get-AzureRemoteAppPlan.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


