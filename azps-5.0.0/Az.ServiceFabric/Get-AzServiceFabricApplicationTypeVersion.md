---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322101"
---
# <span data-ttu-id="31d63-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31d63-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="31d63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31d63-102">SYNOPSIS</span></span>
<span data-ttu-id="31d63-103">Hizmet dokusu uygulama türü sürüm bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="31d63-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="31d63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31d63-104">SYNTAX</span></span>

### <span data-ttu-id="31d63-105">ByResourceGroupAndCluster (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31d63-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31d63-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="31d63-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31d63-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="31d63-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31d63-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="31d63-108">DESCRIPTION</span></span>
<span data-ttu-id="31d63-109">Bu cmdlet 'i, uygulama türü sürüm bilgilerini belirtilen kaynak grubunda ve kümeden almak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="31d63-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="31d63-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31d63-110">EXAMPLES</span></span>

### <span data-ttu-id="31d63-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31d63-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="31d63-112">Bu örnekte, "testAppType" sürüm türü "v1" olan "</span><span class="sxs-lookup"><span data-stu-id="31d63-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="31d63-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="31d63-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="31d63-114">Bu örnekte, belirtilen küme ve tür altında tanımlanan uygulama türü sürümlerinin listesi yer alır.</span><span class="sxs-lookup"><span data-stu-id="31d63-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="31d63-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31d63-115">PARAMETERS</span></span>

### <span data-ttu-id="31d63-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="31d63-116">-ClusterName</span></span>
<span data-ttu-id="31d63-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="31d63-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d63-118">-DefaultProfile</span></span>
<span data-ttu-id="31d63-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31d63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31d63-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="31d63-120">-Name</span></span>
<span data-ttu-id="31d63-121">Uygulama türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="31d63-121">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31d63-122">-ResourceGroupName</span></span>
<span data-ttu-id="31d63-123">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="31d63-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d63-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="31d63-124">-ResourceId</span></span>
<span data-ttu-id="31d63-125">Uygulama türü sürümünün Kolonu.</span><span class="sxs-lookup"><span data-stu-id="31d63-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="31d63-126">-Version</span><span class="sxs-lookup"><span data-stu-id="31d63-126">-Version</span></span>
<span data-ttu-id="31d63-127">Uygulama türünün sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="31d63-127">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d63-128">CommonParameters</span></span>
<span data-ttu-id="31d63-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31d63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d63-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="31d63-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d63-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31d63-131">INPUTS</span></span>

### <span data-ttu-id="31d63-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31d63-132">System.String</span></span>

## <span data-ttu-id="31d63-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31d63-133">OUTPUTS</span></span>

### <span data-ttu-id="31d63-134">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31d63-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="31d63-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31d63-135">NOTES</span></span>

## <span data-ttu-id="31d63-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31d63-136">RELATED LINKS</span></span>
