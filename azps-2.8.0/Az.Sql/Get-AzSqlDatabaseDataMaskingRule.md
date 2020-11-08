---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933682"
---
# <span data-ttu-id="a0061-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0061-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="a0061-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0061-102">SYNOPSIS</span></span>
<span data-ttu-id="a0061-103">Veritabanından veri maskeleme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0061-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="a0061-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0061-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0061-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0061-105">DESCRIPTION</span></span>
<span data-ttu-id="a0061-106">**Get-AzSqlDatabaseDataMaskingRule** cmdlet 'i, BIR Azure SQL veritabanı için belirli bir veri maskeleme kuralı veya tüm veri maskeleme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0061-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="a0061-107">Cmdlet 'i kullanmak için, veritabanını tanımlamak üzere *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini ve bu cmdlet 'In döndürdüğü kuralı belirtmek için *RuleId* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0061-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="a0061-108">*RuleId* belirtmezseniz, bu Azure SQL veritabanı için tüm veri maskeleme kuralları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a0061-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="a0061-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a0061-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0061-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0061-110">EXAMPLES</span></span>

### <span data-ttu-id="a0061-111">Örnek 1: veritabanından tüm veri maskeleme kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="a0061-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="a0061-112">Örnek 2: "dbo" şemasında tanımlanan veri maskeleme kuralını, "Tablo1" ve "Sütun1" sütununu edinin.</span><span class="sxs-lookup"><span data-stu-id="a0061-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="a0061-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0061-113">PARAMETERS</span></span>

### <span data-ttu-id="a0061-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a0061-114">-ColumnName</span></span>
<span data-ttu-id="a0061-115">Maskeleme kuralı tarafından hedeflenen sütunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0061-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="a0061-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0061-116">-DatabaseName</span></span>
<span data-ttu-id="a0061-117">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0061-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a0061-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0061-118">-DefaultProfile</span></span>
<span data-ttu-id="a0061-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0061-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0061-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0061-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0061-121">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0061-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a0061-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a0061-122">-SchemaName</span></span>
<span data-ttu-id="a0061-123">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0061-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="a0061-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0061-124">-ServerName</span></span>
<span data-ttu-id="a0061-125">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0061-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a0061-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="a0061-126">-TableName</span></span>
<span data-ttu-id="a0061-127">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0061-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="a0061-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0061-128">-Confirm</span></span>
<span data-ttu-id="a0061-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0061-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0061-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0061-130">-WhatIf</span></span>
<span data-ttu-id="a0061-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0061-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0061-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0061-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0061-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0061-133">CommonParameters</span></span>
<span data-ttu-id="a0061-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0061-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0061-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0061-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0061-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0061-136">INPUTS</span></span>

### <span data-ttu-id="a0061-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a0061-137">System.String</span></span>

## <span data-ttu-id="a0061-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0061-138">OUTPUTS</span></span>

### <span data-ttu-id="a0061-139">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="a0061-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="a0061-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0061-140">NOTES</span></span>

## <span data-ttu-id="a0061-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0061-141">RELATED LINKS</span></span>

[<span data-ttu-id="a0061-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a0061-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a0061-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0061-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a0061-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0061-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a0061-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a0061-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a0061-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0061-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

