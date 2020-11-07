---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: e0af0c6d741e45c2e00e958342fad940acc2c3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758798"
---
# <span data-ttu-id="b3154-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b3154-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="b3154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3154-102">SYNOPSIS</span></span>
<span data-ttu-id="b3154-103">Veritabanı için veri maskeleme ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3154-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="b3154-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3154-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3154-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3154-105">DESCRIPTION</span></span>
<span data-ttu-id="b3154-106">**Set-AzSqlDatabaseDataMaskingPolicy** cmdlet 'i, BIR Azure SQL veritabanı için veri maskeleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3154-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="b3154-107">Bu cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b3154-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b3154-108">Veri maskeleme işlemlerinin etkin veya devre dışı olduğunu belirtmek için *Datamaskingstate* parametresini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3154-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="b3154-109">Cmdlet başarılı olur ve *geçiş parametresi kullanılırsa* , veritabanı tanımlayıcılarına ek olarak geçerli veri maskeleme ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3154-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="b3154-110">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="b3154-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="b3154-111">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b3154-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b3154-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3154-112">EXAMPLES</span></span>

### <span data-ttu-id="b3154-113">Örnek 1: veritabanı için veri maskeleme ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b3154-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="b3154-114">Bu komut, server01 adındaki sunucudaki database01 adındaki veritabanı için veri maskeleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3154-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="b3154-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3154-115">PARAMETERS</span></span>

### <span data-ttu-id="b3154-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3154-116">-DatabaseName</span></span>
<span data-ttu-id="b3154-117">İlkenin ayarlandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3154-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="b3154-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="b3154-118">-DataMaskingState</span></span>
<span data-ttu-id="b3154-119">Veri maskeleme işleminin etkin veya devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3154-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="b3154-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b3154-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3154-121">Etkin</span><span class="sxs-lookup"><span data-stu-id="b3154-121">Enabled</span></span>
- <span data-ttu-id="b3154-122">Devre dışı varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="b3154-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3154-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3154-123">-DefaultProfile</span></span>
<span data-ttu-id="b3154-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3154-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3154-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b3154-125">-PassThru</span></span>
<span data-ttu-id="b3154-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3154-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3154-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b3154-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3154-128">-Privilegevseçusers</span><span class="sxs-lookup"><span data-stu-id="b3154-128">-PrivilegedUsers</span></span>
<span data-ttu-id="b3154-129">Ayrıcalıklı kullanıcı kimliklerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3154-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="b3154-130">Bu kullanıcıların maskeleme verilerini görüntülemesine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="b3154-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="b3154-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3154-131">-ResourceGroupName</span></span>
<span data-ttu-id="b3154-132">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3154-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b3154-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3154-133">-ServerName</span></span>
<span data-ttu-id="b3154-134">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3154-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="b3154-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3154-135">-Confirm</span></span>
<span data-ttu-id="b3154-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3154-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3154-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3154-137">-WhatIf</span></span>
<span data-ttu-id="b3154-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3154-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3154-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3154-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3154-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3154-140">CommonParameters</span></span>
<span data-ttu-id="b3154-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3154-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3154-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b3154-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3154-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3154-143">INPUTS</span></span>

### <span data-ttu-id="b3154-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b3154-144">System.String</span></span>

## <span data-ttu-id="b3154-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3154-145">OUTPUTS</span></span>

### <span data-ttu-id="b3154-146">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b3154-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="b3154-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3154-147">NOTES</span></span>

## <span data-ttu-id="b3154-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3154-148">RELATED LINKS</span></span>

[<span data-ttu-id="b3154-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b3154-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="b3154-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b3154-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b3154-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b3154-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b3154-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b3154-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b3154-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b3154-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b3154-154">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b3154-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


