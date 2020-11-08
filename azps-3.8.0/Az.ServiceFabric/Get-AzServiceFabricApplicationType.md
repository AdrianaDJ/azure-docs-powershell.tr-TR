---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: dcbb85e9c7b8f1a98acec094043ec03b562e33d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104294"
---
# <span data-ttu-id="eed1d-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eed1d-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="eed1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eed1d-102">SYNOPSIS</span></span>
<span data-ttu-id="eed1d-103">Hizmet dokusu uygulama türü ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="eed1d-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="eed1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eed1d-104">SYNTAX</span></span>

### <span data-ttu-id="eed1d-105">ByResourceGroupAndCluster (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eed1d-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eed1d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eed1d-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eed1d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="eed1d-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eed1d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eed1d-108">DESCRIPTION</span></span>
<span data-ttu-id="eed1d-109">Uygulama türü ayrıntılarını belirtilen kaynak grubunda ve kümeden almak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="eed1d-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="eed1d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eed1d-110">EXAMPLES</span></span>

### <span data-ttu-id="eed1d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eed1d-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="eed1d-112">Bu örnek, uygulama türü ayrıntılarını belirtilen parametrelerle birlikte alır; kaynak bulamazsa bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eed1d-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="eed1d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="eed1d-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="eed1d-114">Bu örnek, belirtilen küme altında tanımlanan uygulama türlerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="eed1d-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="eed1d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eed1d-115">PARAMETERS</span></span>

### <span data-ttu-id="eed1d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eed1d-116">-ClusterName</span></span>
<span data-ttu-id="eed1d-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="eed1d-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eed1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed1d-118">-DefaultProfile</span></span>
<span data-ttu-id="eed1d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eed1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed1d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="eed1d-120">-Name</span></span>
<span data-ttu-id="eed1d-121">Uygulama türünün adını belirtme</span><span class="sxs-lookup"><span data-stu-id="eed1d-121">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eed1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="eed1d-123">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="eed1d-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="eed1d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eed1d-124">-ResourceId</span></span>
<span data-ttu-id="eed1d-125">Uygulama türünün Kolonu.</span><span class="sxs-lookup"><span data-stu-id="eed1d-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="eed1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed1d-126">CommonParameters</span></span>
<span data-ttu-id="eed1d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eed1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed1d-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed1d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed1d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eed1d-129">INPUTS</span></span>

### <span data-ttu-id="eed1d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eed1d-130">System.String</span></span>

## <span data-ttu-id="eed1d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eed1d-131">OUTPUTS</span></span>

### <span data-ttu-id="eed1d-132">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="eed1d-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="eed1d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eed1d-133">NOTES</span></span>

## <span data-ttu-id="eed1d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eed1d-134">RELATED LINKS</span></span>
