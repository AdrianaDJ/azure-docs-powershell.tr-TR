---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319569"
---
# <span data-ttu-id="76828-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="76828-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="76828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76828-102">SYNOPSIS</span></span>
<span data-ttu-id="76828-103">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76828-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="76828-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76828-104">SYNTAX</span></span>

### <span data-ttu-id="76828-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76828-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76828-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76828-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76828-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="76828-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76828-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="76828-108">DESCRIPTION</span></span>
<span data-ttu-id="76828-109">Remove-AzContainerRegistryReplication cmdlet 'i kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76828-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="76828-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76828-110">EXAMPLES</span></span>

### <span data-ttu-id="76828-111">Örnek 1: kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76828-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="76828-112">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76828-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="76828-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76828-113">PARAMETERS</span></span>

### <span data-ttu-id="76828-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76828-114">-DefaultProfile</span></span>
<span data-ttu-id="76828-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76828-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76828-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="76828-116">-Name</span></span>
<span data-ttu-id="76828-117">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="76828-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="76828-118">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="76828-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76828-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="76828-119">-PassThru</span></span>
<span data-ttu-id="76828-120">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="76828-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="76828-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="76828-121">-RegistryName</span></span>
<span data-ttu-id="76828-122">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="76828-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76828-123">-Çoğaltma</span><span class="sxs-lookup"><span data-stu-id="76828-123">-Replication</span></span>
<span data-ttu-id="76828-124">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="76828-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76828-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76828-125">-ResourceGroupName</span></span>
<span data-ttu-id="76828-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="76828-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76828-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="76828-127">-ResourceId</span></span>
<span data-ttu-id="76828-128">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="76828-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76828-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="76828-129">-Confirm</span></span>
<span data-ttu-id="76828-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76828-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76828-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76828-131">-WhatIf</span></span>
<span data-ttu-id="76828-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76828-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76828-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76828-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76828-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76828-134">CommonParameters</span></span>
<span data-ttu-id="76828-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76828-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76828-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76828-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76828-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76828-137">INPUTS</span></span>

### <span data-ttu-id="76828-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="76828-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="76828-139">System. String</span><span class="sxs-lookup"><span data-stu-id="76828-139">System.String</span></span>

## <span data-ttu-id="76828-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76828-140">OUTPUTS</span></span>

### <span data-ttu-id="76828-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76828-141">System.Boolean</span></span>

## <span data-ttu-id="76828-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76828-142">NOTES</span></span>

## <span data-ttu-id="76828-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76828-143">RELATED LINKS</span></span>

[<span data-ttu-id="76828-144">Yeni-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="76828-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="76828-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="76828-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

