---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104291"
---
# <span data-ttu-id="557cc-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="557cc-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="557cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="557cc-102">SYNOPSIS</span></span>
<span data-ttu-id="557cc-103">Hizmet dokusu uygulama ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="557cc-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="557cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="557cc-104">SYNTAX</span></span>

### <span data-ttu-id="557cc-105">ByResourceGroupAndCluster (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="557cc-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="557cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="557cc-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="557cc-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="557cc-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="557cc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="557cc-108">DESCRIPTION</span></span>
<span data-ttu-id="557cc-109">Bu cmdlet, belirtilen kaynak grubundaki ve kümedeki uygulama ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="557cc-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="557cc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="557cc-110">EXAMPLES</span></span>

### <span data-ttu-id="557cc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="557cc-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="557cc-112">Bu örnekte, "testApp" uygulamasının uygulama kaynağı ayrıntıları alınır.</span><span class="sxs-lookup"><span data-stu-id="557cc-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="557cc-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="557cc-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="557cc-114">Bu örnekte, "testCluster" kümesi altındaki uygulamaların listesi yer alır.</span><span class="sxs-lookup"><span data-stu-id="557cc-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="557cc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="557cc-115">PARAMETERS</span></span>

### <span data-ttu-id="557cc-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="557cc-116">-ClusterName</span></span>
<span data-ttu-id="557cc-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="557cc-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="557cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557cc-118">-DefaultProfile</span></span>
<span data-ttu-id="557cc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="557cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557cc-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="557cc-120">-Name</span></span>
<span data-ttu-id="557cc-121">Uygulamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="557cc-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="557cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="557cc-123">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="557cc-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="557cc-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="557cc-124">-ResourceId</span></span>
<span data-ttu-id="557cc-125">Uygulamanın Kolonu.</span><span class="sxs-lookup"><span data-stu-id="557cc-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="557cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557cc-126">CommonParameters</span></span>
<span data-ttu-id="557cc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="557cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557cc-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557cc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557cc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="557cc-129">INPUTS</span></span>

### <span data-ttu-id="557cc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="557cc-130">System.String</span></span>

## <span data-ttu-id="557cc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="557cc-131">OUTPUTS</span></span>

### <span data-ttu-id="557cc-132">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="557cc-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="557cc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="557cc-133">NOTES</span></span>

## <span data-ttu-id="557cc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="557cc-134">RELATED LINKS</span></span>
