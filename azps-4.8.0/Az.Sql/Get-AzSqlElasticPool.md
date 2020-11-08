---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266314"
---
# <span data-ttu-id="a59f8-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a59f8-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="a59f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a59f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a59f8-103">Bir Azure SQL veritabanında esnek havuzlar ve özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="a59f8-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="a59f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a59f8-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a59f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a59f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a59f8-106">**Get-Azsqlelaunpool** cmdlet 'i esnek havuzlar ve bunların özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="a59f8-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="a59f8-107">Yalnızca bu havuzun özellik değerlerini görmek için varolan esnek havuzun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a59f8-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="a59f8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a59f8-108">EXAMPLES</span></span>

### <span data-ttu-id="a59f8-109">Örnek 1: tüm Esnek havuzları alma</span><span class="sxs-lookup"><span data-stu-id="a59f8-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="a59f8-110">Bu komut, server01 adlı sunucudaki tüm Esnek havuzları alır.</span><span class="sxs-lookup"><span data-stu-id="a59f8-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="a59f8-111">Örnek 2: belirli bir esnek havuz edinin</span><span class="sxs-lookup"><span data-stu-id="a59f8-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="a59f8-112">Bu komut, server01 adlı sunucuda ElasticPool0127 adlı elastik havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="a59f8-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="a59f8-113">Örnek 3: Azure SQL esnek veritabanı havuzu için ölçümleri alma</span><span class="sxs-lookup"><span data-stu-id="a59f8-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="a59f8-114">Bu komut, ElasticPool01 adlı bir Azure SQL elastik veritabanı havuzunun ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a59f8-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="a59f8-115">Örnek 4: filtreleme-Elavepoolname "Elana Pool \*" kullanarak tüm Esnek havuzları alma</span><span class="sxs-lookup"><span data-stu-id="a59f8-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="a59f8-116">Bu komut, server01 adlı sunucudaki tüm elastik havuzları "Elaçıkartma" ile başlayan tüm elastik.</span><span class="sxs-lookup"><span data-stu-id="a59f8-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="a59f8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a59f8-117">PARAMETERS</span></span>

### <span data-ttu-id="a59f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a59f8-118">-DefaultProfile</span></span>
<span data-ttu-id="a59f8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a59f8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a59f8-120">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="a59f8-120">-ElasticPoolName</span></span>
<span data-ttu-id="a59f8-121">Bu cmdlet 'in aldığı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a59f8-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a59f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a59f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="a59f8-123">Bu cmdlet 'in aldığı esnek havuzu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a59f8-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a59f8-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a59f8-124">-ServerName</span></span>
<span data-ttu-id="a59f8-125">Bu cmdlet 'in aldığı esnek havuzu içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a59f8-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a59f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59f8-126">CommonParameters</span></span>
<span data-ttu-id="a59f8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a59f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59f8-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a59f8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59f8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a59f8-129">INPUTS</span></span>

### <span data-ttu-id="a59f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a59f8-130">System.String</span></span>

## <span data-ttu-id="a59f8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a59f8-131">OUTPUTS</span></span>

### <span data-ttu-id="a59f8-132">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="a59f8-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a59f8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a59f8-133">NOTES</span></span>

## <span data-ttu-id="a59f8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a59f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="a59f8-135">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a59f8-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="a59f8-136">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a59f8-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="a59f8-137">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a59f8-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


