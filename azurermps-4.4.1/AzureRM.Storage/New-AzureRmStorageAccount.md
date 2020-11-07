---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765024"
---
# New-AzureRmStorageAccount

## SYNOPSIS
Depolama hesabı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-AzureRmStorageAccount** cmdlet 'ı bir Azure depolama hesabı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: depolama hesabı oluşturma
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

Bu komut MyResourceGroup kaynak grubu adı için bir depolama hesabı oluşturur.

### Örnek 2: depolama hizmeti şifrelemesi kullanan bir BLOB depolama hesabı oluşturma
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

Bu komut, etkin erişim türünü kullanan bir BLOB depolama hesabı oluşturur.
Hesap, blob hizmetinde depolama hizmeti şifrelemesini etkinleştirdi.

### Örnek 3: blob ve dosya hizmetlerinde depolama hizmeti şifrelemesini sağlayan bir depolama hesabı oluşturun ve Azure Keykasa için bir kimlik oluşturun ve atayın.
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

Bu komut, blob ve dosya hizmetlerinde depolama hizmeti şifrelemesini destekleyen bir depolama hesabı oluşturur.  Ayrıca, Azure Keykasası aracılığıyla hesap anahtarlarını yönetmek için kullanılabilecek bir kimlik oluşturur ve bunu atar.

## PARAMETRELERINE

### -AccessTier
Bu cmdlet 'in oluşturduğu depolama hesabının erişim katmanını belirtir.
Bu parametre için kabul edilebilir değerler: kolay ve serin.

*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.

Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Atama kimliği
Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Custometkialanıadı
Depolama hesabının özel etki alanı adını belirtir.
Varsayılan değer depolama alanıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini etkinleştirilip etkinleştirilmediğini gösterir.
Azure Blob ve Azure dosya hizmetleri destekleniyor.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Depolama hesabının https trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Type: System.Management.Automation.ActionPreference
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
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Bu cmdlet 'in oluşturduğu depolama hesabı türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Alanını.
Blob, tablo, kuyruk, dosya ve disklerin depolanmasını destekleyen genel amaçlı depolama hesabı.
 
- BlobStorage.
Yalnızca blob depolamasını destekleyen BLOB depolama hesabı.
 

Varsayılan değer depolama alanıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Oluşturulacak depolama hesabının konumunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Oluşturulacak depolama hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
Depolama hesabı ağ kuralı kümesi

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Depolama hesabının ekleneceği kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Bu cmdlet 'in oluşturduğu depolama hesabının SKU adını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Standard_LRS.
Yerel olarak yedekli depolama. 
- Standard_ZRS.
Bölge ile yedekli depolama.
- Standard_GRS.
Coğrafi olarak yedekli depolama. 
- Standard_RAGRS.
Okuma erişimi coğrafi depolama. 
- Premium_LRS.
Premium yerel olarak yedekli depolama.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
*Tür* parametresi Için blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.

Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Usealt etki alanı
Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)


