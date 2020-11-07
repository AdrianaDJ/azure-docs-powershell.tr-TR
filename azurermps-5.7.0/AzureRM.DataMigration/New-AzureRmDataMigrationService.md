---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764457"
---
# New-AzureRmDataMigrationService

## SYNOPSIS
Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## Tanım
New-AzureRmDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin yeni bir örneğini oluşturur. Bu cmdlet, var olan Azure Resource grubunun adını, Azure veritabanı geçiş hizmeti 'nin yeni örneğinin oluşturulması için benzersiz adı, örneğin sağlandıkları bölgeyi, DMS çalışan SKU 'nun adını ve hizmetin bulunacağı Azure sanal alt ağının adını alır. Abonelik adında parametre yoksa, kullanıcının Azure oturumu açma oturumunun varsayılan aboneliğini belirtmesi veya Get-AzureRmSubscription-SubscriptionName "MySubscription" | Başka bir abonelik seçmek için Select-AzureRmSubscription.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

Yukarıdaki örnekte, Merkezi ABD bölgesindeki TestService adlı Azure veritabanı geçiş hizmeti örneğinin nasıl oluşturulacağı gösterilmektedir.


## PARAMETRELERINE

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

### -Konum
Oluşturulacak Azure veritabanı geçiş hizmeti örneğinin konumu, bir Azure bölgesine karşılık gelir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HizmetAdı
Azure veritabanı geçiş hizmeti örneğinin adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Azure veritabanı geçiş hizmeti örneğinin SKU 'su. Şu anda olası değerler Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Virtualsubnetıd
Azure veritabanı geçiş hizmeti örneğinde kullanılacak sanal ağın altındaki alt ağın adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## ÇıKıŞLAR

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

