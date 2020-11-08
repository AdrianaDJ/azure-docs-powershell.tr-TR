---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: bba2ab235532f83b3955ff9a12016438e0e1960e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097162"
---
# <span data-ttu-id="e805c-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e805c-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="e805c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e805c-102">SYNOPSIS</span></span>
<span data-ttu-id="e805c-103">Service Fabric 'ı kümeden bir uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="e805c-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="e805c-104">Bu, bu kaynağın altındaki tüm tür sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e805c-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="e805c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e805c-105">SYNTAX</span></span>

### <span data-ttu-id="e805c-106">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e805c-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e805c-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e805c-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e805c-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e805c-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e805c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e805c-109">DESCRIPTION</span></span>
<span data-ttu-id="e805c-110">Bu cmdlet, kümeyi oluşturan bir uygulama türünü kaldırır ve bu kaynağın altındaki tüm tür sürümünü kaldırır, ancak bu komutu çalıştırmadan önce tüm uygulamalar kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e805c-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="e805c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e805c-111">EXAMPLES</span></span>

### <span data-ttu-id="e805c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e805c-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="e805c-113">Bu örnekte, "testAppType" uygulama türü ve altındaki tüm sürüm kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="e805c-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="e805c-114">Bu türle oluşturulmuş uygulamalar varsa komut bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e805c-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="e805c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e805c-115">PARAMETERS</span></span>

### <span data-ttu-id="e805c-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e805c-116">-ClusterName</span></span>
<span data-ttu-id="e805c-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e805c-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e805c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e805c-118">-DefaultProfile</span></span>
<span data-ttu-id="e805c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e805c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e805c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e805c-120">-Force</span></span>
<span data-ttu-id="e805c-121">Sormadan kaldır.</span><span class="sxs-lookup"><span data-stu-id="e805c-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="e805c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e805c-122">-InputObject</span></span>
<span data-ttu-id="e805c-123">Uygulama türü kaynağı.</span><span class="sxs-lookup"><span data-stu-id="e805c-123">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e805c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e805c-124">-Name</span></span>
<span data-ttu-id="e805c-125">Uygulama türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e805c-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e805c-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e805c-126">-PassThru</span></span>
<span data-ttu-id="e805c-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="e805c-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e805c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e805c-128">-ResourceGroupName</span></span>
<span data-ttu-id="e805c-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e805c-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e805c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e805c-130">-ResourceId</span></span>
<span data-ttu-id="e805c-131">Uygulama türünün Kolonu.</span><span class="sxs-lookup"><span data-stu-id="e805c-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="e805c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e805c-132">-Confirm</span></span>
<span data-ttu-id="e805c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e805c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e805c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e805c-134">-WhatIf</span></span>
<span data-ttu-id="e805c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e805c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e805c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e805c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e805c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e805c-137">CommonParameters</span></span>
<span data-ttu-id="e805c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e805c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e805c-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e805c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e805c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e805c-140">INPUTS</span></span>

### <span data-ttu-id="e805c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e805c-141">System.String</span></span>

### <span data-ttu-id="e805c-142">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="e805c-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="e805c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e805c-143">OUTPUTS</span></span>

### <span data-ttu-id="e805c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e805c-144">System.Boolean</span></span>

## <span data-ttu-id="e805c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e805c-145">NOTES</span></span>

## <span data-ttu-id="e805c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e805c-146">RELATED LINKS</span></span>
