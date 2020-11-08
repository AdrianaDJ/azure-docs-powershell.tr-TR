---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: e9f248575d0f5193a11c729384e674870b3de29c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097170"
---
# <span data-ttu-id="3a967-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a967-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="3a967-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a967-102">SYNOPSIS</span></span>
<span data-ttu-id="3a967-103">Kümeden bir uygulamayı kaldırma.</span><span class="sxs-lookup"><span data-stu-id="3a967-103">Remove an application from the cluster.</span></span> <span data-ttu-id="3a967-104">Bu işlem, uygulamanın altındaki tüm hizmetleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a967-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="3a967-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a967-105">SYNTAX</span></span>

### <span data-ttu-id="3a967-106">ByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a967-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a967-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3a967-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a967-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a967-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a967-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a967-109">DESCRIPTION</span></span>
<span data-ttu-id="3a967-110">Bu cmdlet, kümedeki bir uygulamayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a967-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="3a967-111">Bu işlem, varsa uygulama kaynağının altındaki tüm hizmetleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a967-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="3a967-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a967-112">EXAMPLES</span></span>

### <span data-ttu-id="3a967-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a967-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="3a967-114">Bu örnekte, "testRG" kaynak grubunun altındaki "testApp" uygulaması ve "testCluster" uygulaması kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3a967-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="3a967-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a967-115">PARAMETERS</span></span>

### <span data-ttu-id="3a967-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3a967-116">-ClusterName</span></span>
<span data-ttu-id="3a967-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3a967-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3a967-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a967-118">-DefaultProfile</span></span>
<span data-ttu-id="3a967-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a967-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a967-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3a967-120">-Force</span></span>
<span data-ttu-id="3a967-121">Sormadan kaldır.</span><span class="sxs-lookup"><span data-stu-id="3a967-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="3a967-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a967-122">-InputObject</span></span>
<span data-ttu-id="3a967-123">Uygulama kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3a967-123">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a967-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a967-124">-Name</span></span>
<span data-ttu-id="3a967-125">Uygulamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3a967-125">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a967-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a967-126">-PassThru</span></span>
<span data-ttu-id="3a967-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="3a967-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3a967-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a967-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a967-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3a967-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3a967-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a967-130">-ResourceId</span></span>
<span data-ttu-id="3a967-131">Uygulamanın Kolonu.</span><span class="sxs-lookup"><span data-stu-id="3a967-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="3a967-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a967-132">-Confirm</span></span>
<span data-ttu-id="3a967-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a967-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a967-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a967-134">-WhatIf</span></span>
<span data-ttu-id="3a967-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a967-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a967-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a967-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a967-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a967-137">CommonParameters</span></span>
<span data-ttu-id="3a967-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a967-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a967-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a967-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a967-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a967-140">INPUTS</span></span>

### <span data-ttu-id="3a967-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3a967-141">System.String</span></span>

### <span data-ttu-id="3a967-142">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="3a967-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3a967-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a967-143">OUTPUTS</span></span>

### <span data-ttu-id="3a967-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a967-144">System.Boolean</span></span>

## <span data-ttu-id="3a967-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a967-145">NOTES</span></span>

## <span data-ttu-id="3a967-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a967-146">RELATED LINKS</span></span>
