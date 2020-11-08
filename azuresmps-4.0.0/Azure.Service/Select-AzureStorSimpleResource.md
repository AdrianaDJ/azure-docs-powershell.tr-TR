---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105448"
---
# Select-AzureStorSimpleResource

## SYNOPSIS
Kaynağı geçerli kaynak olarak ayarlar.

## INDEKI

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Select-AzureStorSimpleResource** cmdlet 'i geçerli kaynak olarak bir kaynak ayarlar.
Bir kaynak seçtikten sonra, bu kaynak bağlamında diğer cmdlet 'ler uygulanır.

## ÖRNEKLERDEN

### Örnek 1: bir kaynağı ilk kez seçme
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Bu komut, Contoso64-Tsqa adlı kaynağı geçerli bağlam olarak seçer.
Bu örnekte, bilgisayar daha önce bu içeriği başlatmış ve dolayısıyla, *Registrationkey* parametresi için bir değer belirtmelisiniz.

### Örnek 2: kaynak seçme girişimi
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### Örnek 3: daha önce seçili bir kaynağı seçme
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Bu komut, Contoso64-Tsqa adlı kaynağı geçerli bağlam olarak seçer.
Bu örnekte, bu bağlam daha önce seçilmiştir ve bu nedenle, *Registrationkey* parametresi için bir değer belirtmeniz gerekmez.

## PARAMETRELERINE

### -Profil
Bir Azure profili belirtir.

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

### -RegistrationKey
Bir kayıt anahtarı belirtir.
İlk kez kaynak seçtiğinizde bir anahtar belirtin.
Bu cmdlet geçerli kaynağı seçtikten sonra cmdlet 'ler bu anahtarı gerektiği gibi kullanır.
Daha fazla bilgi için, [bkz](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) .

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

### -ResourceName
Geçerli kaynak olarak seçilecek kaynağın adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### StorSimpleResourceContext
Bu cmdlet, kaynak bağlamının ayrıntılarını içeren bir **Storsimpleresourcecontext** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


