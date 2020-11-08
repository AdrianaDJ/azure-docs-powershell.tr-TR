---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108727"
---
# <span data-ttu-id="4f156-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="4f156-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="4f156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f156-102">SYNOPSIS</span></span>
<span data-ttu-id="4f156-103">Yönetilen küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4f156-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="4f156-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f156-104">SYNTAX</span></span>

### <span data-ttu-id="4f156-105">BySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f156-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f156-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f156-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f156-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4f156-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f156-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f156-108">DESCRIPTION</span></span>
<span data-ttu-id="4f156-109">Yönetilen küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4f156-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="4f156-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f156-110">EXAMPLES</span></span>

### <span data-ttu-id="4f156-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f156-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="4f156-112">Küme ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4f156-112">Get cluster details.</span></span>

### <span data-ttu-id="4f156-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4f156-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="4f156-114">Belirtilen kaynak grubu altındaki kümelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="4f156-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="4f156-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4f156-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="4f156-116">Geçerli aboneliğin altındaki kümelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="4f156-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="4f156-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f156-117">PARAMETERS</span></span>

### <span data-ttu-id="4f156-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f156-118">-DefaultProfile</span></span>
<span data-ttu-id="4f156-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f156-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f156-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f156-120">-Name</span></span>
<span data-ttu-id="4f156-121">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4f156-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f156-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f156-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f156-123">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4f156-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f156-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f156-124">CommonParameters</span></span>
<span data-ttu-id="4f156-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f156-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f156-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f156-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f156-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f156-127">INPUTS</span></span>

### <span data-ttu-id="4f156-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4f156-128">System.String</span></span>

## <span data-ttu-id="4f156-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f156-129">OUTPUTS</span></span>

### <span data-ttu-id="4f156-130">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="4f156-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="4f156-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f156-131">NOTES</span></span>

## <span data-ttu-id="4f156-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f156-132">RELATED LINKS</span></span>
