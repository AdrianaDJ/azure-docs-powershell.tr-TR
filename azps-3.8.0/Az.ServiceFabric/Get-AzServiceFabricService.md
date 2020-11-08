---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 62f1e4a9313ebcbd2ad6d815344dc18e5844ed13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097201"
---
# <span data-ttu-id="5c2fa-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5c2fa-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="5c2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2fa-103">Belirtilen uygulama ve kümenin altındaki hizmet Fabric hizmeti ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="5c2fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c2fa-104">SYNTAX</span></span>

### <span data-ttu-id="5c2fa-105">ByResourceGroupAndCluster (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c2fa-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c2fa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5c2fa-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c2fa-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="5c2fa-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c2fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c2fa-108">DESCRIPTION</span></span>
<span data-ttu-id="5c2fa-109">Bu cmdlet, belirtilen uygulama ve kümedeki hizmet ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="5c2fa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c2fa-110">EXAMPLES</span></span>

### <span data-ttu-id="5c2fa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5c2fa-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="5c2fa-112">Bu örnekte, "testApp ~ testService" hizmetinin hizmet kaynağı ayrıntıları alınır.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="5c2fa-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5c2fa-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="5c2fa-114">Bu örnekte, "testApp" uygulamasının altındaki hizmetlerin listesi yer alır.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="5c2fa-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c2fa-115">PARAMETERS</span></span>

### <span data-ttu-id="5c2fa-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="5c2fa-116">-ApplicationName</span></span>
<span data-ttu-id="5c2fa-117">Uygulamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-117">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2fa-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5c2fa-118">-ClusterName</span></span>
<span data-ttu-id="5c2fa-119">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5c2fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2fa-120">-DefaultProfile</span></span>
<span data-ttu-id="5c2fa-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2fa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c2fa-122">-Name</span></span>
<span data-ttu-id="5c2fa-123">Hizmetin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-123">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c2fa-125">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5c2fa-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5c2fa-126">-ResourceId</span></span>
<span data-ttu-id="5c2fa-127">Hizmetin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="5c2fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2fa-128">CommonParameters</span></span>
<span data-ttu-id="5c2fa-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2fa-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c2fa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2fa-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c2fa-131">INPUTS</span></span>

### <span data-ttu-id="5c2fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c2fa-132">System.String</span></span>

## <span data-ttu-id="5c2fa-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c2fa-133">OUTPUTS</span></span>

### <span data-ttu-id="5c2fa-134">Microsoft. Azure. Commands. ServiceFabric. modeller. PSService</span><span class="sxs-lookup"><span data-stu-id="5c2fa-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="5c2fa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c2fa-135">NOTES</span></span>

## <span data-ttu-id="5c2fa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c2fa-136">RELATED LINKS</span></span>
