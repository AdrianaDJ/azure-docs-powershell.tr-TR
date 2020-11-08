---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1475296638cec105713eaa390bcce6552e5502ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108724"
---
# <span data-ttu-id="1b4d3-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1b4d3-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="1b4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4d3-103">Kümeden bir hizmeti kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="1b4d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b4d3-104">SYNTAX</span></span>

### <span data-ttu-id="1b4d3-105">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b4d3-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b4d3-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="1b4d3-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b4d3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1b4d3-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b4d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b4d3-108">DESCRIPTION</span></span>
<span data-ttu-id="1b4d3-109">Bu cmdlet, kümenin bir hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="1b4d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b4d3-110">EXAMPLES</span></span>

### <span data-ttu-id="1b4d3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b4d3-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="1b4d3-112">Bu örnekte "testApp ~ testService1" hizmeti kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="1b4d3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b4d3-113">PARAMETERS</span></span>

### <span data-ttu-id="1b4d3-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1b4d3-114">-ApplicationName</span></span>
<span data-ttu-id="1b4d3-115">Uygulamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-115">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1b4d3-116">-ClusterName</span></span>
<span data-ttu-id="1b4d3-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4d3-118">-DefaultProfile</span></span>
<span data-ttu-id="1b4d3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b4d3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1b4d3-120">-Force</span></span>
<span data-ttu-id="1b4d3-121">Sormadan kaldır.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-121">Remove without prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b4d3-122">-InputObject</span></span>
<span data-ttu-id="1b4d3-123">Hizmet kaynağı.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-123">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b4d3-124">-Name</span></span>
<span data-ttu-id="1b4d3-125">Hizmetin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-125">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1b4d3-126">-PassThru</span></span>
<span data-ttu-id="1b4d3-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="1b4d3-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="1b4d3-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1b4d3-130">-ResourceId</span></span>
<span data-ttu-id="1b4d3-131">Hizmetin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="1b4d3-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b4d3-132">-Confirm</span></span>
<span data-ttu-id="1b4d3-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b4d3-134">-WhatIf</span></span>
<span data-ttu-id="1b4d3-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b4d3-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4d3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4d3-137">CommonParameters</span></span>
<span data-ttu-id="1b4d3-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4d3-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b4d3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4d3-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b4d3-140">INPUTS</span></span>

### <span data-ttu-id="1b4d3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1b4d3-141">System.String</span></span>

### <span data-ttu-id="1b4d3-142">Microsoft. Azure. Commands. ServiceFabric. modeller. PSService</span><span class="sxs-lookup"><span data-stu-id="1b4d3-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="1b4d3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b4d3-143">OUTPUTS</span></span>

### <span data-ttu-id="1b4d3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b4d3-144">System.Boolean</span></span>

## <span data-ttu-id="1b4d3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b4d3-145">NOTES</span></span>

## <span data-ttu-id="1b4d3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b4d3-146">RELATED LINKS</span></span>
