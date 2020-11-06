---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7b4d445ede7bae59431707f3ff6bc587effde21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591547"
---
# <span data-ttu-id="3bd5d-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3bd5d-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="3bd5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd5d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd5d-103">Azure SQL esnek havuz Danışmanı 'nın otomatik yürütme durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bd5d-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bd5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bd5d-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd5d-106">**Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet 'ı Azure SQL esnek havuz Danışmanı için otomatik yürütme özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="3bd5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bd5d-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd5d-108">Örnek 1: bir danışman için otomatik çalıştırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3bd5d-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="3bd5d-109">Bu komut, CreateIndex adındaki bir Advisor 'ın otomatik yürütme durumunu etkin olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="3bd5d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bd5d-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd5d-111">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="3bd5d-111">-AdvisorName</span></span>
<span data-ttu-id="3bd5d-112">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği bir danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="3bd5d-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3bd5d-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="3bd5d-114">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği yeni bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="3bd5d-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3bd5d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3bd5d-116">Etkin</span><span class="sxs-lookup"><span data-stu-id="3bd5d-116">Enabled</span></span>
- <span data-ttu-id="3bd5d-117">DISABLED</span><span class="sxs-lookup"><span data-stu-id="3bd5d-117">Disabled</span></span>
- <span data-ttu-id="3bd5d-118">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="3bd5d-118">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd5d-119">-DefaultProfile</span></span>
<span data-ttu-id="3bd5d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3bd5d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bd5d-121">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="3bd5d-121">-ElasticPoolName</span></span>
<span data-ttu-id="3bd5d-122">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="3bd5d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd5d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3bd5d-124">Bu esnek havuzu içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="3bd5d-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3bd5d-125">-ServerName</span></span>
<span data-ttu-id="3bd5d-126">Elastik havuzun bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="3bd5d-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="3bd5d-127">-Confirm</span></span>
<span data-ttu-id="3bd5d-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd5d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd5d-129">-WhatIf</span></span>
<span data-ttu-id="3bd5d-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd5d-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd5d-132">CommonParameters</span></span>
<span data-ttu-id="3bd5d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd5d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd5d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd5d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bd5d-135">INPUTS</span></span>

### <span data-ttu-id="3bd5d-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3bd5d-136">None</span></span>
<span data-ttu-id="3bd5d-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3bd5d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bd5d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bd5d-138">OUTPUTS</span></span>

### <span data-ttu-id="3bd5d-139">Microsoft. Azure. Commands. Sql. Advisor. model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3bd5d-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="3bd5d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bd5d-140">NOTES</span></span>
* <span data-ttu-id="3bd5d-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, SQL, elastik havuz, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="3bd5d-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="3bd5d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bd5d-142">RELATED LINKS</span></span>

[<span data-ttu-id="3bd5d-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3bd5d-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3bd5d-144">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="3bd5d-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
