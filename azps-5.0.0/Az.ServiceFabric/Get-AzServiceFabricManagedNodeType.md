---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322093"
---
# <span data-ttu-id="93e46-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="93e46-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="93e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e46-102">SYNOPSIS</span></span>
<span data-ttu-id="93e46-103">Yönetilen düğüm türü kaynak ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="93e46-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="93e46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93e46-104">SYNTAX</span></span>

### <span data-ttu-id="93e46-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93e46-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93e46-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93e46-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93e46-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93e46-107">DESCRIPTION</span></span>
<span data-ttu-id="93e46-108">Yönetilen düğüm türü kaynak ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="93e46-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="93e46-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93e46-109">EXAMPLES</span></span>

### <span data-ttu-id="93e46-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="93e46-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="93e46-111">Düğüm türü ayrıntıları alma.</span><span class="sxs-lookup"><span data-stu-id="93e46-111">Get node type details.</span></span>

### <span data-ttu-id="93e46-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="93e46-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="93e46-113">Belirtilen kümenin altındaki düğüm türlerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="93e46-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="93e46-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93e46-114">PARAMETERS</span></span>

### <span data-ttu-id="93e46-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="93e46-115">-ClusterName</span></span>
<span data-ttu-id="93e46-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="93e46-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="93e46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e46-117">-DefaultProfile</span></span>
<span data-ttu-id="93e46-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93e46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e46-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="93e46-119">-Name</span></span>
<span data-ttu-id="93e46-120">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="93e46-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e46-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e46-121">-ResourceGroupName</span></span>
<span data-ttu-id="93e46-122">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="93e46-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="93e46-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e46-123">CommonParameters</span></span>
<span data-ttu-id="93e46-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93e46-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e46-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="93e46-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e46-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93e46-126">INPUTS</span></span>

### <span data-ttu-id="93e46-127">System. String</span><span class="sxs-lookup"><span data-stu-id="93e46-127">System.String</span></span>

## <span data-ttu-id="93e46-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93e46-128">OUTPUTS</span></span>

### <span data-ttu-id="93e46-129">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="93e46-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="93e46-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93e46-130">NOTES</span></span>

## <span data-ttu-id="93e46-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93e46-131">RELATED LINKS</span></span>
