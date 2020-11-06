---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586714"
---
# Remove-AzureRmDataLakeStoreItemAclEntry

## SYNOPSIS
Data Lake Store 'da bir dosyanın veya klasörün ACL 'sinden girdiyi kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### RemoveByACLObject (varsayılan)
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveSpecificACE
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEN (ACL) bir GIRIŞI (ACE) kaldırır.

## ÖRNEKLERDEN

### Örnek 1: Kullanıcı girdisini kaldırma
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

Bu komut, ContosoADL hesabından Patti Tamlarından Kullanıcı ACE 'sini kaldırır.

## PARAMETRELERINE

### -Hesap
Data Lake Store hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AceType
Kaldırılacak ACE türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Kullanıcıların
- Gruplandır
- Mayı
- Diğerini

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ACL
Kaldırılacak girdileri içeren ACL nesnesini belirtir.

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Varsayılan
Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi kaldırmadığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
ACE 'yi kaldırmak için AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Kök dizinden (/) başlayarak ACE 'yi kaldırmak istediğiniz öğenin veri Lake Store yolunu belirtir.

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### DataLakeStoreItemAce[]
' ACL ' parametresi ardışık düzen için ' DataLakeStoreItemAce [] ' türünün değerini kabul eder

## ÇıKıŞLAR

### bool
Geçiş belirtildiyse, başarılı bir tamamlandığında doğru sonucunu döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRmDataLakeStoreItemAclEntry](./Set-AzureRmDataLakeStoreItemAclEntry.md)


