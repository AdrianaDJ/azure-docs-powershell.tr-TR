---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: bf82ca7804ecd3f382728217395be234155e9035
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589667"
---
# Add-AzureRmSqlServerKeyVaultKey

## SYNOPSIS
SQL sunucusuna bir anahtar kasa anahtarı ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Add-AzureRmSqlServerKeyVaultKey cmdlet 'i, sağlanan SQL sunucusuna bir anahtar kasa anahtarı ekler.
Sunucuda kasaya ' Get, wrapKey, unwrapKey ' izinleri bulunmalıdır.

## ÖRNEKLERDEN

### Örnek 1: Anahtar Kasası ekleme anahtarı
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Bu komut, ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' ContosoServer ' ADLı SQL sunucusuna kimliği ' ' olan Anahtar Kasası anahtarını ekler.

ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın
```yaml
Type: SwitchParameter
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

### -KeyId
Azure Anahtar Kasası tuş kimliği.

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

### -ResourceGroupName
Kaynak grubunun adı

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

### -ServerName
Azure SQL Server adı.

```yaml
Type: String
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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. model. azures, Serverkeyvaultkeymodel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)
