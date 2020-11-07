---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: ee9bc55bef1491bbf07da96380802cec185bfb49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932426"
---
# <span data-ttu-id="b5151-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b5151-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="b5151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5151-102">SYNOPSIS</span></span>
<span data-ttu-id="b5151-103">Service Fabric 'ı kümeden bir uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="b5151-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="b5151-104">Bu, bu kaynağın altındaki tüm tür sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5151-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="b5151-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5151-105">SYNTAX</span></span>

### <span data-ttu-id="b5151-106">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5151-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5151-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b5151-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5151-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5151-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5151-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5151-109">DESCRIPTION</span></span>
<span data-ttu-id="b5151-110">Bu cmdlet, kümeyi oluşturan bir uygulama türünü kaldırır ve bu kaynağın altındaki tüm tür sürümünü kaldırır, ancak bu komutu çalıştırmadan önce tüm uygulamalar kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b5151-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="b5151-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5151-111">EXAMPLES</span></span>

### <span data-ttu-id="b5151-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5151-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="b5151-113">Bu örnekte, "testAppType" uygulama türü ve altındaki tüm sürüm kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="b5151-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="b5151-114">Bu türle oluşturulmuş uygulamalar varsa komut bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5151-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="b5151-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5151-115">PARAMETERS</span></span>

### <span data-ttu-id="b5151-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5151-116">-ClusterName</span></span>
<span data-ttu-id="b5151-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5151-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b5151-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5151-118">-DefaultProfile</span></span>
<span data-ttu-id="b5151-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5151-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5151-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b5151-120">-Force</span></span>
<span data-ttu-id="b5151-121">Sormadan kaldır.</span><span class="sxs-lookup"><span data-stu-id="b5151-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="b5151-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5151-122">-InputObject</span></span>
<span data-ttu-id="b5151-123">Uygulama türü kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b5151-123">The application type resource.</span></span>

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

### <span data-ttu-id="b5151-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5151-124">-Name</span></span>
<span data-ttu-id="b5151-125">Uygulama türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5151-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="b5151-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b5151-126">-PassThru</span></span>
<span data-ttu-id="b5151-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b5151-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b5151-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5151-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5151-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5151-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b5151-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b5151-130">-ResourceId</span></span>
<span data-ttu-id="b5151-131">Uygulama türünün Kolonu.</span><span class="sxs-lookup"><span data-stu-id="b5151-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="b5151-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5151-132">-Confirm</span></span>
<span data-ttu-id="b5151-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5151-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5151-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5151-134">-WhatIf</span></span>
<span data-ttu-id="b5151-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5151-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5151-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5151-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5151-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5151-137">CommonParameters</span></span>
<span data-ttu-id="b5151-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5151-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5151-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5151-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5151-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5151-140">INPUTS</span></span>

### <span data-ttu-id="b5151-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b5151-141">System.String</span></span>

### <span data-ttu-id="b5151-142">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="b5151-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="b5151-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5151-143">OUTPUTS</span></span>

### <span data-ttu-id="b5151-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5151-144">System.Boolean</span></span>

## <span data-ttu-id="b5151-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5151-145">NOTES</span></span>

## <span data-ttu-id="b5151-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5151-146">RELATED LINKS</span></span>
