---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107400"
---
# New-WAPackQuickVM

## SYNOPSIS
Şablona dayalı bir sanal makine oluşturur.

## INDEKI

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Yeni-WAPackQuickVM** cmdlet 'i, şablona dayalı bir sanal makine oluşturur.

## ÖRNEKLERDEN

### Örnek 1: şablona dayalı sanal makine oluşturma
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

İlk komut bir **PSCredential** nesnesi oluşturur ve $Credentials değişkeninde depolar.
Cmdlet bir hesap ve parola sorar.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .

İkinci komut **Get-WAPackVMTemplate** cmdlet 'ini kullanarak bir şablon alır.
Komut, şablonun KIMLIĞINI belirtir.
Komut, şablon nesnesini $TemplateID değişkeninde depolar.

Son komutu, VirtualMachine023 adlı bir sanal makine oluşturur.
Komut, $TemplateId depolanan şablondaki sanal makineyi temel alır.

## PARAMETRELERINE

### -Ad
Sanal makine için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

### -Şablon
Şablon belirtir.
Cmdlet, belirttiğiniz şablona göre bir sanal makine oluşturur.
Şablon nesnesi edinmek için **Get-WAPackVMTemplate** cmdlet 'ini kullanın.

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Yerel yönetici hesabının kimlik bilgilerini belirtir.
**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

[Yeni-WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


