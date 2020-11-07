---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916163"
---
# <span data-ttu-id="dc1d8-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="dc1d8-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="dc1d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1d8-103">Kaynak grubundaki tüm kusto kümelerini listeler veya belirli bir kusto kümesi edinin.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="dc1d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc1d8-104">SYNTAX</span></span>

### <span data-ttu-id="dc1d8-105">ByClusterOrResourceGroupOrSubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dc1d8-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc1d8-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="dc1d8-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc1d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc1d8-107">DESCRIPTION</span></span>
<span data-ttu-id="dc1d8-108">Kaynak grubundaki tüm kusto kümelerini listeler veya belirli bir kusto kümesi edinin.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="dc1d8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc1d8-109">EXAMPLES</span></span>

### <span data-ttu-id="dc1d8-110">Örnek 1-kaynak grubundaki tüm kusto kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="dc1d8-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="dc1d8-111">Tür: Microsoft. kusto/küme kimliği:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg adı: mykustocluster1 konumu: Orta ABD kapasitesi: 3 SKU: D13_v2 ProvisioningState: başarılı durum: {} https://mykustocluster1.centralus.kusto.windows.nethttps://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="dc1d8-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="dc1d8-112">Tür: Microsoft. kusto/küme kimliği:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg adı: mykustocluster2 konumu: Orta ABD kapasitesi: 5 SKU: D13_v2 ProvisioningState: başarılı durum: {} https://mykustocluster2.centralus.kusto.windows.nethttps://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="dc1d8-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="dc1d8-113">Yukarıdaki komut, "testrg" kaynak grubundaki tüm kusto kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="dc1d8-114">Örnek 2-ada göre belirli bir kusto kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="dc1d8-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="dc1d8-115">Yukarıdaki komut, "testrg" kaynak grubunda "mykustocluster" adlı kusto kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="dc1d8-116">Örnek 3-kaynak kimliğiyle belirli bir kusto kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="dc1d8-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="dc1d8-117">Yukarıdaki komut, "testrg" kaynak grubunda "mykustocluster" adlı kusto kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="dc1d8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc1d8-118">PARAMETERS</span></span>

### <span data-ttu-id="dc1d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1d8-119">-DefaultProfile</span></span>
<span data-ttu-id="dc1d8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc1d8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc1d8-121">-Name</span></span>
<span data-ttu-id="dc1d8-122">Belirli bir kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc1d8-124">Kullanıcının kümeyi almasını istediği kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="dc1d8-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dc1d8-125">-ResourceId</span></span>
<span data-ttu-id="dc1d8-126">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="dc1d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1d8-127">CommonParameters</span></span>
<span data-ttu-id="dc1d8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1d8-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1d8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1d8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc1d8-130">INPUTS</span></span>

### <span data-ttu-id="dc1d8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dc1d8-131">System.String</span></span>

## <span data-ttu-id="dc1d8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc1d8-132">OUTPUTS</span></span>

### <span data-ttu-id="dc1d8-133">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="dc1d8-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="dc1d8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc1d8-134">NOTES</span></span>

## <span data-ttu-id="dc1d8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc1d8-135">RELATED LINKS</span></span>
