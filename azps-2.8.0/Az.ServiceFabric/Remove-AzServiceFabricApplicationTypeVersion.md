---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 74398a027a7ec9de916640b39834cb1045cfe1a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933189"
---
# <span data-ttu-id="8edd6-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8edd6-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="8edd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8edd6-102">SYNOPSIS</span></span>
<span data-ttu-id="8edd6-103">Hizmet yapısı 'nı kümeden uygulama türü sürümü.</span><span class="sxs-lookup"><span data-stu-id="8edd6-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="8edd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8edd6-104">SYNTAX</span></span>

### <span data-ttu-id="8edd6-105">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8edd6-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8edd6-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8edd6-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8edd6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8edd6-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8edd6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8edd6-108">DESCRIPTION</span></span>
<span data-ttu-id="8edd6-109">Bu cmdlet, Service Fabric 'ı kümeden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8edd6-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="8edd6-110">Bu komutu çalıştırmadan önce bu kaynağın altındaki tüm uygulamalar kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8edd6-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="8edd6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8edd6-111">EXAMPLES</span></span>

### <span data-ttu-id="8edd6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8edd6-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="8edd6-113">Bu örnekte, "testAppType" türünün altındaki "v1" sürümü kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="8edd6-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="8edd6-114">Bu kaynak altında herhangi bir uygulama vardır komut bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8edd6-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="8edd6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8edd6-115">PARAMETERS</span></span>

### <span data-ttu-id="8edd6-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8edd6-116">-ClusterName</span></span>
<span data-ttu-id="8edd6-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8edd6-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8edd6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8edd6-118">-DefaultProfile</span></span>
<span data-ttu-id="8edd6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8edd6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8edd6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8edd6-120">-Force</span></span>
<span data-ttu-id="8edd6-121">Sormadan kaldır.</span><span class="sxs-lookup"><span data-stu-id="8edd6-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="8edd6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8edd6-122">-InputObject</span></span>
<span data-ttu-id="8edd6-123">Uygulama türü sürümü kaynağı.</span><span class="sxs-lookup"><span data-stu-id="8edd6-123">The application type version resource.</span></span>

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

### <span data-ttu-id="8edd6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8edd6-124">-Name</span></span>
<span data-ttu-id="8edd6-125">Uygulama türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8edd6-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="8edd6-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8edd6-126">-PassThru</span></span>
<span data-ttu-id="8edd6-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="8edd6-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8edd6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8edd6-128">-ResourceGroupName</span></span>
<span data-ttu-id="8edd6-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8edd6-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8edd6-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8edd6-130">-ResourceId</span></span>
<span data-ttu-id="8edd6-131">Uygulama türü sürümünün Kolonu.</span><span class="sxs-lookup"><span data-stu-id="8edd6-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="8edd6-132">-Version</span><span class="sxs-lookup"><span data-stu-id="8edd6-132">-Version</span></span>
<span data-ttu-id="8edd6-133">Uygulama türü sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="8edd6-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="8edd6-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="8edd6-134">-Confirm</span></span>
<span data-ttu-id="8edd6-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8edd6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8edd6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8edd6-136">-WhatIf</span></span>
<span data-ttu-id="8edd6-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8edd6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8edd6-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8edd6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8edd6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8edd6-139">CommonParameters</span></span>
<span data-ttu-id="8edd6-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8edd6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8edd6-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8edd6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8edd6-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8edd6-142">INPUTS</span></span>

### <span data-ttu-id="8edd6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8edd6-143">System.String</span></span>

### <span data-ttu-id="8edd6-144">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8edd6-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="8edd6-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8edd6-145">OUTPUTS</span></span>

### <span data-ttu-id="8edd6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8edd6-146">System.Boolean</span></span>

## <span data-ttu-id="8edd6-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8edd6-147">NOTES</span></span>

## <span data-ttu-id="8edd6-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8edd6-148">RELATED LINKS</span></span>