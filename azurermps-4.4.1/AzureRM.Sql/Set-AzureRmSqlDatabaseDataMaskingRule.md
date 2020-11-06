---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587738"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## SYNOPSIS
Veritabanı için veri maskeleme kuralı özelliklerini ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme kuralı ayarlar.
Cmdlet 'i kullanmak için, kuralı belirlemek üzere *Resourcegroupname* , *ServerName* , *DatabaseName* ve *RuleId* parametrelerini sağlayın.
Kuralı yeniden uygulamak için *SchemaName* , *TableName* ve *ColumnName* parametrelerinden herhangi birini sağlayabilirsiniz.
Verilerin maskelenme biçimini değiştirmek için *Maskingişlevi* parametresini belirtin.

*Maskingişlevi* Için bir sayı veya metin değeri belirtirseniz, sayı maskeleme için sayı veya sayı veya *NumberFrom* metin maskeleme için *PrefixSize* , *replacementstring* ve *soneboyutu* *parametrelerini belirtebilirsiniz* .
Komut başarılı olur ve *geçiş parametresini belirtirseniz* cmdlet, veri maskeleme kuralı özelliklerini ve kural tanımlayıcılarını tanımlayan bir nesne döndürür.
Kural tanımlayıcıları, **Resourcegroupname** , **ServerName** , **DatabaseName** ve **RuleId** ile sınırlı değildir.

Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.

## ÖRNEKLERDEN

### Örnek 1: veritabanında veri maskeleme kuralı aralığını değiştirme
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Bu komut, Rule17 KIMLIĞINE sahip bir veri maskeleme kuralını değiştirir.
Bu kural, Database01 adındaki veritabanında server01.
Bu komut, maskelenmiş değer olarak rastgele bir sayının üretildiği aralığın sınırlarını değiştirir.
Yeni Aralık 23 ile 42 arasındadır.

## PARAMETRELERINE

### -ColumnName
Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Veritabanının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Maskingişlevi
Kuralın kullandığı maskeleme işlevini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Varsayýlan
- Not
- Metinleri
- Numarasıyla
- SocialSecurityNumber
- CreditCardNumber
- E-posta

Varsayılan değer varsayılandır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Rastgele bir değer seçilen aralığın alt sınır numarasını belirtir.
Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.
Varsayılan değer 0 ' dır.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Rastgele bir değer seçilen aralığın üst sınır numarasını belirtir.
Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir sayı değeri belirtmeniz durumunda belirtin.
Varsayılan değer 0 ' dır.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

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

### -PrefixSize
Metnin başındaki metnin başındaki karakter sayısını belirtir.
Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.
Varsayılan değer 0 ' dır.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplacementString
Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.
Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.
Varsayılan değer 0 ' dır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Veritabanının atandığı kaynak grubunun adını belirtir.

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

### -SchemaName
Şemanın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Veritabanını barındıran sunucunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Soneboyut
Metin düzeyinde, maskelenmeyen karakter sayısını belirtir.
Bu parametreyi yalnızca *Maskingişlevi* parametresi Için bir metin değeri belirtmeniz durumunda belirtin.
Varsayılan değer 0 ' dır.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableName
Maskelenmiş sütununu içeren veritabanı tablosunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

###  
Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. Security. model. DatabaseDataMaskingRuleModel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[New-AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)


