---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106395"
---
# Add-AzureCertificate

## SYNOPSIS
Bir Azure bulut hizmetine sertifika yükler.

## INDEKI

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Add-Azurecercertificate** . cmdlet 'ı bir Azure hizmeti için sertifika yükler.

## ÖRNEKLERDEN

### Örnek 1: sertifikayı ve parolayı karşıya yükleme
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

Bu komut, bir bulut hizmetine ContosoCertificate. pfx sertifika dosyasını yükler.
Komut, sertifikanın parolasını belirtir.

### Örnek 2: sertifika dosyası yükleme
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

Bu komut, bir bulut hizmetine ContosoCertificate. cer sertifika dosyasını yükler.
Komut, sertifikanın parolasını belirtir.

### Örnek 3: sertifika nesnesi yükleme
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

İlk komut, Windows PowerShell çekirdek **Get-Item** cmdlet 'ini kullanarak bir Kullanıcı mağazasından bir sertifika alır.
Komut, sertifikayı $Certificate değişkeninde depolar.

İkinci komut $certificate sertifikayı bir bulut hizmetine yükler.

## PARAMETRELERINE

### -CertToDeploy
Dağıtılacak sertifikayı belirtir.
*. Cer veya * içeren dosya gibi bir sertifika dosyasının tam yolunu belirtebilirsiniz.
pfx dosya adı uzantısı veya X. 509.440 sertifika nesnesi.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parola
Sertifika parolasını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -HizmetAdı
Bu cmdlet 'in sertifika eklediği Azure hizmetinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### ManagementOperationContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurecercertificate](./Get-AzureCertificate.md)

[New-Azurecercertificate Atesetting](./New-AzureCertificateSetting.md)

[Remove-Azurecercertificate](./Remove-AzureCertificate.md)


