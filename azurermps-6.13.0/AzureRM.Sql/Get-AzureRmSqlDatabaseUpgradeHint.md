---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b289dc637b3d75321120f06eb9ddf604ebcdabba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763429"
---
# <span data-ttu-id="f7639-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="f7639-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="f7639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7639-102">SYNOPSIS</span></span>
<span data-ttu-id="f7639-103">Bir veritabanı için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f7639-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7639-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7639-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7639-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7639-105">DESCRIPTION</span></span>
<span data-ttu-id="f7639-106">**Get-AzureRmSqlDatabaseUpgradeHint** cmdlet 'i, BIR Azure SQL veritabanını yükseltmek için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f7639-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="f7639-107">Hala Web ve Iş fiyatlandırması katmanlarındaki veritabanları, yeni temel, standart veya Premium fiyatlandırma katmanlarına yükseltme ipucunu alır.</span><span class="sxs-lookup"><span data-stu-id="f7639-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="f7639-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="f7639-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f7639-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7639-109">EXAMPLES</span></span>

### <span data-ttu-id="f7639-110">Örnek 1: sunucudaki tüm veritabanlarına yönelik öneriler alma</span><span class="sxs-lookup"><span data-stu-id="f7639-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f7639-111">Bu komut, server01 adındaki sunucudaki tüm veritabanlarının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f7639-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="f7639-112">Örnek 2: belirli veritabanı için öneriler alma</span><span class="sxs-lookup"><span data-stu-id="f7639-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f7639-113">Bu komut, belirli bir veritabanının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f7639-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="f7639-114">Örnek 3: elastik bir veritabanı havuzunda bulunmayan tüm veritabanları için öneri alma</span><span class="sxs-lookup"><span data-stu-id="f7639-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="f7639-115">Bu komut, elastik bir veritabanı havuzunda olmayan tüm veritabanlarının yükseltme ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f7639-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="f7639-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7639-116">PARAMETERS</span></span>

### <span data-ttu-id="f7639-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f7639-117">-DatabaseName</span></span>
<span data-ttu-id="f7639-118">Bu cmdlet 'in bir yükseltme ipucu aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7639-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="f7639-119">Bir veritabanı belirtmezseniz, bu cmdlet mantıksal sunucudaki tüm veritabanlarının ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f7639-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="f7639-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7639-120">-DefaultProfile</span></span>
<span data-ttu-id="f7639-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f7639-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7639-122">-Excludeeladapooladaylar</span><span class="sxs-lookup"><span data-stu-id="f7639-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="f7639-123">Elastik veritabanı havuzlarındaki veritabanlarının döndürülen önerilerden dışlanıp dışlanmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7639-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="f7639-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7639-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7639-125">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7639-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f7639-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7639-126">-ServerName</span></span>
<span data-ttu-id="f7639-127">Bu cmdlet 'in yükseltme ipucu aldığı veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7639-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="f7639-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7639-128">-Confirm</span></span>
<span data-ttu-id="f7639-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7639-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7639-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7639-130">-WhatIf</span></span>
<span data-ttu-id="f7639-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7639-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7639-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7639-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7639-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7639-133">CommonParameters</span></span>
<span data-ttu-id="f7639-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7639-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7639-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7639-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7639-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7639-136">INPUTS</span></span>

### <span data-ttu-id="f7639-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f7639-137">System.String</span></span>

### <span data-ttu-id="f7639-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7639-138">System.Boolean</span></span>

## <span data-ttu-id="f7639-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7639-139">OUTPUTS</span></span>

### <span data-ttu-id="f7639-140">Microsoft. Azure. Management. Sql. LegacySdk. modeller. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="f7639-140">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="f7639-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7639-141">NOTES</span></span>

## <span data-ttu-id="f7639-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7639-142">RELATED LINKS</span></span>

[<span data-ttu-id="f7639-143">Get-Azurermsqldatabasegenişletilen</span><span class="sxs-lookup"><span data-stu-id="f7639-143">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="f7639-144">Get-Azurermsqlelakpoolönerisi</span><span class="sxs-lookup"><span data-stu-id="f7639-144">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


