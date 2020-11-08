---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: f50baca10d3079ac800b694670ce2b4c8c85fc84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097159"
---
# <span data-ttu-id="b7583-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b7583-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="b7583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7583-102">SYNOPSIS</span></span>
<span data-ttu-id="b7583-103">Hizmet yapısı 'nı kümeden uygulama türü sürümü.</span><span class="sxs-lookup"><span data-stu-id="b7583-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="b7583-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7583-104">SYNTAX</span></span>

### <span data-ttu-id="b7583-105">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7583-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7583-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b7583-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7583-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7583-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7583-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7583-108">DESCRIPTION</span></span>
<span data-ttu-id="b7583-109">Bu cmdlet, Service Fabric 'ı kümeden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b7583-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="b7583-110">Bu komutu çalıştırmadan önce bu kaynağın altındaki tüm uygulamalar kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7583-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="b7583-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7583-111">EXAMPLES</span></span>

### <span data-ttu-id="b7583-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7583-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="b7583-113">Bu örnekte, "testAppType" türünün altındaki "v1" sürümü kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b7583-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="b7583-114">Bu kaynak altında herhangi bir uygulama vardır komut bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7583-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="b7583-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7583-115">PARAMETERS</span></span>

### <span data-ttu-id="b7583-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7583-116">-ClusterName</span></span>
<span data-ttu-id="b7583-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b7583-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b7583-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7583-118">-DefaultProfile</span></span>
<span data-ttu-id="b7583-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7583-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7583-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b7583-120">-Force</span></span>
<span data-ttu-id="b7583-121">Sormadan kaldır.</span><span class="sxs-lookup"><span data-stu-id="b7583-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="b7583-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7583-122">-InputObject</span></span>
<span data-ttu-id="b7583-123">Uygulama türü sürümü kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b7583-123">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7583-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7583-124">-Name</span></span>
<span data-ttu-id="b7583-125">Uygulama türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b7583-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7583-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b7583-126">-PassThru</span></span>
<span data-ttu-id="b7583-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b7583-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b7583-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7583-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7583-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b7583-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b7583-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b7583-130">-ResourceId</span></span>
<span data-ttu-id="b7583-131">Uygulama türü sürümünün Kolonu.</span><span class="sxs-lookup"><span data-stu-id="b7583-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="b7583-132">-Version</span><span class="sxs-lookup"><span data-stu-id="b7583-132">-Version</span></span>
<span data-ttu-id="b7583-133">Uygulama türü sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="b7583-133">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7583-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7583-134">-Confirm</span></span>
<span data-ttu-id="b7583-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7583-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7583-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7583-136">-WhatIf</span></span>
<span data-ttu-id="b7583-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7583-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7583-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7583-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7583-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7583-139">CommonParameters</span></span>
<span data-ttu-id="b7583-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7583-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7583-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7583-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7583-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7583-142">INPUTS</span></span>

### <span data-ttu-id="b7583-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b7583-143">System.String</span></span>

### <span data-ttu-id="b7583-144">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b7583-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="b7583-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7583-145">OUTPUTS</span></span>

### <span data-ttu-id="b7583-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7583-146">System.Boolean</span></span>

## <span data-ttu-id="b7583-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7583-147">NOTES</span></span>

## <span data-ttu-id="b7583-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7583-148">RELATED LINKS</span></span>
