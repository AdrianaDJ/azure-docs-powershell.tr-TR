---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 6e24eaee77e8965ea34cbfcd8c169d675bce56d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096612"
---
# <span data-ttu-id="71e7d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="71e7d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="71e7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="71e7d-103">Kaynak grubundaki tüm kusto kümelerini listeler veya belirli bir kusto kümesi edinin.</span><span class="sxs-lookup"><span data-stu-id="71e7d-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="71e7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71e7d-104">SYNTAX</span></span>

### <span data-ttu-id="71e7d-105">ByClusterOrResourceGroupOrSubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71e7d-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71e7d-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="71e7d-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e7d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="71e7d-107">DESCRIPTION</span></span>
<span data-ttu-id="71e7d-108">Kaynak grubundaki tüm kusto kümelerini listeler veya belirli bir kusto kümesi edinin.</span><span class="sxs-lookup"><span data-stu-id="71e7d-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="71e7d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71e7d-109">EXAMPLES</span></span>

### <span data-ttu-id="71e7d-110">Örnek 1-kaynak grubundaki tüm kusto kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="71e7d-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="71e7d-111">Tür: Microsoft. kusto/küme kimliği:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg adı: mykustocluster1 konumu: Orta ABD kapasitesi: 3 SKU: D13_v2 ProvisioningState: başarılı durum: {} https://mykustocluster1.centralus.kusto.windows.nethttps://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="71e7d-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="71e7d-112">Tür: Microsoft. kusto/küme kimliği:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg adı: mykustocluster2 konumu: Orta ABD kapasitesi: 5 SKU: D13_v2 ProvisioningState: başarılı durum: {} https://mykustocluster2.centralus.kusto.windows.nethttps://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="71e7d-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="71e7d-113">Yukarıdaki komut, "testrg" kaynak grubundaki tüm kusto kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="71e7d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="71e7d-114">Örnek 2-ada göre belirli bir kusto kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="71e7d-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="71e7d-115">Yukarıdaki komut, "testrg" kaynak grubunda "mykustocluster" adlı kusto kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="71e7d-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="71e7d-116">Örnek 3-kaynak kimliğiyle belirli bir kusto kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="71e7d-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="71e7d-117">Yukarıdaki komut, "testrg" kaynak grubunda "mykustocluster" adlı kusto kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="71e7d-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="71e7d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71e7d-118">PARAMETERS</span></span>

### <span data-ttu-id="71e7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e7d-119">-DefaultProfile</span></span>
<span data-ttu-id="71e7d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71e7d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e7d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="71e7d-121">-Name</span></span>
<span data-ttu-id="71e7d-122">Belirli bir kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="71e7d-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="71e7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="71e7d-124">Kullanıcının kümeyi almasını istediği kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="71e7d-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="71e7d-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="71e7d-125">-ResourceId</span></span>
<span data-ttu-id="71e7d-126">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="71e7d-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="71e7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e7d-127">CommonParameters</span></span>
<span data-ttu-id="71e7d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71e7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e7d-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e7d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e7d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71e7d-130">INPUTS</span></span>

### <span data-ttu-id="71e7d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="71e7d-131">System.String</span></span>

## <span data-ttu-id="71e7d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71e7d-132">OUTPUTS</span></span>

### <span data-ttu-id="71e7d-133">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="71e7d-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="71e7d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71e7d-134">NOTES</span></span>

## <span data-ttu-id="71e7d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71e7d-135">RELATED LINKS</span></span>
