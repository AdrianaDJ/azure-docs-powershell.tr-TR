---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d33635cd3876a3426c3db96489d623d0a61f1d03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592383"
---
# Start-AzureRmSqlServerUpgrade

## SYNOPSIS
SQL veritabanı sunucusunu yükseltmeyi başlatır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Start-AzureRmSqlServerUpgrade** cmdlet 'ı, Azure SQL veritabanı sunucusu sürüm 11 ' i sürüm 12 ' ye yükseltmeyi başlatır.
Get-AzureRmSqlServerUpgrade cmdlet 'ini kullanarak yükseltmenin ilerlemesini izleyebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sunucuyu yükseltme
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Bu komut, server01 adlı sunucuyu kaynak grubuna atanmış olarak yükseltir.

### Örnek 2: zamanlamayı zamanla ve veritabanı önerisi kullanarak sunucuyu yükseltme
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

İlk komut, Get-Date cmdlet 'ini kullanarak gelecekte beş dakikalık bir saat oluşturur.
Komut $ScheduleTime değişkende depolar.
Daha fazla bilgi için yazın `Get-Help Get-Date` .

İkinci komut bir **RecommendedDatabaseProperties** nesnesi oluşturur ve bu nesneyi $DatabaseMap değişkende depolar.

Sonraki üç komut, $DatabaseMap depolanan nesnenin özelliklerine değerler atar.

Son komut, server01 adındaki var olan sunucuyu 12,0 sürümüne yükseltir.
$ScheduleTime değişkeninde belirtildiği gibi, komutu çalıştırdıktan sonraki en erken saat beş dakikadır.
Yükseltmenin ardından, veritabanı contosodb standart sürümü çalıştırmaya başlar ve hizmet düzeyi amacını S0 olur.

## PARAMETRELERINE

### -DatabaseCollection
Bu cmdlet 'in sunucu yükseltmesinde kullandığı bir **RecommendedDatabaseProperties** nesneleri dizisini belirtir.

```yaml
Type: RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Elaafcollection
Sunucu yükseltmesinde kullanılacak bir **yükseltilebilir Dereyorumdedelaçıkartpoolproperties** nesneleri dizisi belirtir.

```yaml
Type: UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sunucunun atandığı kaynak grubunun adını belirtir.

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

### -ScheduleUpgradeAfterUtcDateTime
Sunucuyu yükseltebileceğiniz en erken zamanı bir **DateTime** nesnesi olarak belirtir.
ISO8601 biçiminde, Eşgüdümlü Evrensel Saat (UTC) cinsinden bir değer belirtin.
Daha fazla bilgi için yazın `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Bu cmdlet 'in yükselttiğinde sunucunun adını belirtir.

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

### -ServerVersion
Bu cmdlet 'in sunucuyu yükselttiğinde sürümü belirtir.
Geçerli tek değer 12,0 ' dır.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. ServerUpgrade. model. azures, Serverupgrademodel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Stop-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)


