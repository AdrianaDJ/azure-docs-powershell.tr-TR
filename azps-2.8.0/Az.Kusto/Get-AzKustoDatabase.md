---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751587"
---
# <span data-ttu-id="4ba07-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="4ba07-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="4ba07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba07-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba07-103">Kümedeki tüm kusto veritabanlarını listeler veya belirli bir kusto veritabanı edinin.</span><span class="sxs-lookup"><span data-stu-id="4ba07-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="4ba07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ba07-104">SYNTAX</span></span>

### <span data-ttu-id="4ba07-105">ByClusterOrResourceGroupOrSubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ba07-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ba07-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4ba07-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ba07-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ba07-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ba07-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ba07-108">DESCRIPTION</span></span>
<span data-ttu-id="4ba07-109">Kümedeki tüm kusto veritabanlarını listeler veya belirli bir kusto veritabanı edinin.</span><span class="sxs-lookup"><span data-stu-id="4ba07-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="4ba07-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ba07-110">EXAMPLES</span></span>

### <span data-ttu-id="4ba07-111">Örnek 1-ada göre kümedeki tüm kusto veritabanlarını listeler</span><span class="sxs-lookup"><span data-stu-id="4ba07-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="4ba07-112">Yukarıdaki komut, "mykustocluster" kaynak grubunda bulunan "" kümesindeki tüm kusto veritabanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="4ba07-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="4ba07-113">Örnek 2-boru tarafından kümedeki tüm kusto veritabanlarını listeler</span><span class="sxs-lookup"><span data-stu-id="4ba07-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="4ba07-114">Yukarıdaki komut cmdlet 'i kullanarak "mykustocluster" kaynak grubunda bulunan "" adlı kusto kümesini alır `Get-AzKustoCluster` ve `Get-AzKustoDatabase` Bu kümedeki tüm veritabanlarını listelemek için sonucu cmdlet 'e yöneltecektir.</span><span class="sxs-lookup"><span data-stu-id="4ba07-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="4ba07-115">Örnek 3-adla belirli bir kusto veritabanı alma</span><span class="sxs-lookup"><span data-stu-id="4ba07-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="4ba07-116">Yukarıdaki komut, "mykustodatabase" adlı kusto veritabanını, "testrg" kaynak grubunda bulunan "mykustocluster" kümesinde döndürür.</span><span class="sxs-lookup"><span data-stu-id="4ba07-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="4ba07-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ba07-117">PARAMETERS</span></span>

### <span data-ttu-id="4ba07-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4ba07-118">-ClusterName</span></span>
<span data-ttu-id="4ba07-119">Veritabanının mevcut olduğu kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="4ba07-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba07-120">-DefaultProfile</span></span>
<span data-ttu-id="4ba07-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ba07-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba07-122">-InputObject</span></span>
<span data-ttu-id="4ba07-123">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4ba07-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba07-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ba07-124">-Name</span></span>
<span data-ttu-id="4ba07-125">veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4ba07-125">the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba07-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba07-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ba07-127">Kullanıcının kümeyi almasını istediği kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4ba07-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba07-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4ba07-128">-ResourceId</span></span>
<span data-ttu-id="4ba07-129">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4ba07-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba07-130">CommonParameters</span></span>
<span data-ttu-id="4ba07-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ba07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba07-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba07-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba07-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ba07-133">INPUTS</span></span>

### <span data-ttu-id="4ba07-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba07-134">System.String</span></span>

### <span data-ttu-id="4ba07-135">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4ba07-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4ba07-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ba07-136">OUTPUTS</span></span>

### <span data-ttu-id="4ba07-137">Microsoft. Azure. Commands. kusto. modeller. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="4ba07-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="4ba07-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ba07-138">NOTES</span></span>

## <span data-ttu-id="4ba07-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ba07-139">RELATED LINKS</span></span>
