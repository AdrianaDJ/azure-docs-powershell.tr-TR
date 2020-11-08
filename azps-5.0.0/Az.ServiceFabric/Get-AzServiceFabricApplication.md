---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: c282ea9e902f26d010c2421339de68bc670e2f35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275249"
---
# <span data-ttu-id="a08d2-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a08d2-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="a08d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a08d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a08d2-103">Hizmet dokusu uygulama ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="a08d2-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="a08d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a08d2-104">SYNTAX</span></span>

### <span data-ttu-id="a08d2-105">ByResourceGroupAndCluster (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a08d2-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a08d2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a08d2-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a08d2-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a08d2-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a08d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a08d2-108">DESCRIPTION</span></span>
<span data-ttu-id="a08d2-109">Bu cmdlet, belirtilen kaynak grubundaki ve kümedeki uygulama ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a08d2-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="a08d2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a08d2-110">EXAMPLES</span></span>

### <span data-ttu-id="a08d2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a08d2-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="a08d2-112">Bu örnekte, "testApp" uygulamasının uygulama kaynağı ayrıntıları alınır.</span><span class="sxs-lookup"><span data-stu-id="a08d2-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="a08d2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a08d2-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="a08d2-114">Bu örnekte, "testCluster" kümesi altındaki uygulamaların listesi yer alır.</span><span class="sxs-lookup"><span data-stu-id="a08d2-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="a08d2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a08d2-115">PARAMETERS</span></span>

### <span data-ttu-id="a08d2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a08d2-116">-ClusterName</span></span>
<span data-ttu-id="a08d2-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a08d2-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a08d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08d2-118">-DefaultProfile</span></span>
<span data-ttu-id="a08d2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a08d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08d2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a08d2-120">-Name</span></span>
<span data-ttu-id="a08d2-121">Uygulamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a08d2-121">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a08d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a08d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="a08d2-123">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a08d2-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a08d2-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a08d2-124">-ResourceId</span></span>
<span data-ttu-id="a08d2-125">Uygulamanın Kolonu.</span><span class="sxs-lookup"><span data-stu-id="a08d2-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="a08d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08d2-126">CommonParameters</span></span>
<span data-ttu-id="a08d2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a08d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08d2-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a08d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08d2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a08d2-129">INPUTS</span></span>

### <span data-ttu-id="a08d2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a08d2-130">System.String</span></span>

## <span data-ttu-id="a08d2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a08d2-131">OUTPUTS</span></span>

### <span data-ttu-id="a08d2-132">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a08d2-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="a08d2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a08d2-133">NOTES</span></span>

## <span data-ttu-id="a08d2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a08d2-134">RELATED LINKS</span></span>
