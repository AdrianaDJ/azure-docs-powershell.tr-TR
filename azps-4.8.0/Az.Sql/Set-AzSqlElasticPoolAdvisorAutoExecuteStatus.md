---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266773"
---
# <span data-ttu-id="da743-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da743-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="da743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da743-102">SYNOPSIS</span></span>
<span data-ttu-id="da743-103">Azure SQL esnek havuz Danışmanı 'nın otomatik yürütme durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da743-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="da743-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da743-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da743-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da743-105">DESCRIPTION</span></span>
<span data-ttu-id="da743-106">**Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet 'ı Azure SQL esnek havuz Danışmanı için otomatik yürütme özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="da743-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="da743-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da743-107">EXAMPLES</span></span>

### <span data-ttu-id="da743-108">Örnek 1: bir danışman için otomatik çalıştırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="da743-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="da743-109">Bu komut, CreateIndex adındaki bir Advisor 'ın otomatik yürütme durumunu etkin olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="da743-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="da743-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da743-110">PARAMETERS</span></span>

### <span data-ttu-id="da743-111">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="da743-111">-AdvisorName</span></span>
<span data-ttu-id="da743-112">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği bir danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da743-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="da743-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da743-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="da743-114">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği yeni bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="da743-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="da743-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="da743-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da743-116">Etkin</span><span class="sxs-lookup"><span data-stu-id="da743-116">Enabled</span></span>
- <span data-ttu-id="da743-117">DISABLED</span><span class="sxs-lookup"><span data-stu-id="da743-117">Disabled</span></span>
- <span data-ttu-id="da743-118">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="da743-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da743-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da743-119">-DefaultProfile</span></span>
<span data-ttu-id="da743-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="da743-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da743-121">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="da743-121">-ElasticPoolName</span></span>
<span data-ttu-id="da743-122">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da743-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="da743-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da743-123">-ResourceGroupName</span></span>
<span data-ttu-id="da743-124">Bu esnek havuzu içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da743-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="da743-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da743-125">-ServerName</span></span>
<span data-ttu-id="da743-126">Elastik havuzun bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da743-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="da743-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="da743-127">-Confirm</span></span>
<span data-ttu-id="da743-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da743-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da743-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da743-129">-WhatIf</span></span>
<span data-ttu-id="da743-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da743-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da743-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da743-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da743-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da743-132">CommonParameters</span></span>
<span data-ttu-id="da743-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da743-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da743-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="da743-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da743-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da743-135">INPUTS</span></span>

### <span data-ttu-id="da743-136">System. String</span><span class="sxs-lookup"><span data-stu-id="da743-136">System.String</span></span>

### <span data-ttu-id="da743-137">Microsoft. Azure. Commands. Sql. Advisor. cmdlet. danışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="da743-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="da743-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da743-138">OUTPUTS</span></span>

### <span data-ttu-id="da743-139">Microsoft. Azure. Commands. Sql. Advisor. model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="da743-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="da743-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da743-140">NOTES</span></span>
* <span data-ttu-id="da743-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, SQL, elastik havuz, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="da743-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="da743-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da743-142">RELATED LINKS</span></span>

[<span data-ttu-id="da743-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="da743-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="da743-144">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="da743-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
