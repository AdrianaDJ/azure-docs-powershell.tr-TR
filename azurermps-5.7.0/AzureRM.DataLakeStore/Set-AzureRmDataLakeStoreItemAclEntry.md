---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587557"
---
# Set-AzureRmDataLakeStoreItemAclEntry

## SYNOPSIS
Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SetByACLObject (varsayılan)
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSpecificACE
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDEKI (ACL) GIRIŞINI (ACE) değiştirir.

## ÖRNEKLERDEN

### Örnek 1: ACE için izinleri değiştirme
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

Bu komut, Patti Tamleri'nin ACE 'sini tüm izinlere sahip olacak şekilde değiştirir.

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
Değiştirilecek ACE türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Kullanıcıların 
- Gruplandır 
- Mayı 
- Diğerini

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ACL
Değiştirilecek girdileri içeren ACL nesnesini belirtir.

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Varsayılan
Bu işlemin belirtilen ACL 'den varsayılan ACE 'yi değiştirdiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
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
ACE 'sinin değiştirileceği AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.

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
Kök dizinden (/) başlayarak ACE 'yi değiştirecek olan öğenin veri Lake Store yolunu belirtir.

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

### -İzinler
ACE izinlerini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yabilirsiniz
- Execute
- Yazmaktır
- WriteExecute
- Okuması
- Readex
- Yazma
- Tüm

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
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

### 'A<DataLakeStoreItemAce>
Geçiş belirtildiyse, sonuç olarak ACL girişlerinin sonuç listesi döndürülür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureRmDataLakeStoreItemAclEntry](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


