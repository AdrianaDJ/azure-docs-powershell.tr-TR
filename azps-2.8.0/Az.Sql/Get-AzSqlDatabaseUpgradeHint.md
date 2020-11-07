---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933649"
---
# <span data-ttu-id="e23ae-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="e23ae-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="e23ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e23ae-102">SYNOPSIS</span></span>
<span data-ttu-id="e23ae-103">Bir veritabanı için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e23ae-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="e23ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e23ae-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e23ae-105">DESCRIPTION</span></span>
<span data-ttu-id="e23ae-106">**Get-AzSqlDatabaseUpgradeHint** cmdlet 'i, BIR Azure SQL veritabanını yükseltmek için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e23ae-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="e23ae-107">Hala Web ve Iş fiyatlandırması katmanlarındaki veritabanları, yeni temel, standart veya Premium fiyatlandırma katmanlarına yükseltme ipucunu alır.</span><span class="sxs-lookup"><span data-stu-id="e23ae-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="e23ae-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e23ae-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e23ae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e23ae-109">EXAMPLES</span></span>

### <span data-ttu-id="e23ae-110">Örnek 1: sunucudaki tüm veritabanlarına yönelik öneriler alma</span><span class="sxs-lookup"><span data-stu-id="e23ae-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e23ae-111">Bu komut, server01 adındaki sunucudaki tüm veritabanlarının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e23ae-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="e23ae-112">Örnek 2: belirli veritabanı için öneriler alma</span><span class="sxs-lookup"><span data-stu-id="e23ae-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e23ae-113">Bu komut, belirli bir veritabanının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e23ae-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="e23ae-114">Örnek 3: elastik bir veritabanı havuzunda bulunmayan tüm veritabanları için öneri alma</span><span class="sxs-lookup"><span data-stu-id="e23ae-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="e23ae-115">Bu komut, elastik bir veritabanı havuzunda olmayan tüm veritabanlarının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e23ae-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="e23ae-116">Örnek 4: filtreleme kullanarak sunucudaki tüm veritabanlarına yönelik öneriler alma</span><span class="sxs-lookup"><span data-stu-id="e23ae-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="e23ae-117">Bu komut, server01 adlı sunucudaki "veritabanı" ile başlayan tüm veritabanlarının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e23ae-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="e23ae-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e23ae-118">PARAMETERS</span></span>

### <span data-ttu-id="e23ae-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e23ae-119">-DatabaseName</span></span>
<span data-ttu-id="e23ae-120">Bu cmdlet 'in bir yükseltme ipucu aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e23ae-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="e23ae-121">Bir veritabanı belirtmezseniz, bu cmdlet mantıksal sunucudaki tüm veritabanlarının ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e23ae-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e23ae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23ae-122">-DefaultProfile</span></span>
<span data-ttu-id="e23ae-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e23ae-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e23ae-124">-Excludeeladapooladaylar</span><span class="sxs-lookup"><span data-stu-id="e23ae-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="e23ae-125">Elastik veritabanı havuzlarındaki veritabanlarının döndürülen önerilerden dışlanıp dışlanmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e23ae-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="e23ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="e23ae-127">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e23ae-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e23ae-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e23ae-128">-ServerName</span></span>
<span data-ttu-id="e23ae-129">Bu cmdlet 'in yükseltme ipucu aldığı veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e23ae-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="e23ae-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e23ae-130">-Confirm</span></span>
<span data-ttu-id="e23ae-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e23ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e23ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23ae-132">-WhatIf</span></span>
<span data-ttu-id="e23ae-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e23ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e23ae-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e23ae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e23ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23ae-135">CommonParameters</span></span>
<span data-ttu-id="e23ae-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e23ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23ae-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e23ae-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23ae-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e23ae-138">INPUTS</span></span>

### <span data-ttu-id="e23ae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e23ae-139">System.String</span></span>

### <span data-ttu-id="e23ae-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e23ae-140">System.Boolean</span></span>

## <span data-ttu-id="e23ae-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e23ae-141">OUTPUTS</span></span>

### <span data-ttu-id="e23ae-142">Microsoft. Azure. Management. Sql. LegacySdk. modeller. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="e23ae-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="e23ae-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e23ae-143">NOTES</span></span>

## <span data-ttu-id="e23ae-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e23ae-144">RELATED LINKS</span></span>

[<span data-ttu-id="e23ae-145">Get-Azsqldatabasegenişletilen</span><span class="sxs-lookup"><span data-stu-id="e23ae-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="e23ae-146">Get-Azsqlelaunpooltavsiyeleri</span><span class="sxs-lookup"><span data-stu-id="e23ae-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


