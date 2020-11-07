---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 717e1ecd7b2242ee5643ca80883e472f5ea4a3c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752595"
---
# <span data-ttu-id="951b8-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="951b8-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="951b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="951b8-102">SYNOPSIS</span></span>
<span data-ttu-id="951b8-103">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="951b8-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="951b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="951b8-104">SYNTAX</span></span>

### <span data-ttu-id="951b8-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="951b8-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951b8-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="951b8-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951b8-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="951b8-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="951b8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="951b8-108">DESCRIPTION</span></span>
<span data-ttu-id="951b8-109">Remove-AzContainerRegistryReplication cmdlet 'i kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="951b8-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="951b8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="951b8-110">EXAMPLES</span></span>

### <span data-ttu-id="951b8-111">Örnek 1: kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="951b8-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="951b8-112">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="951b8-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="951b8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="951b8-113">PARAMETERS</span></span>

### <span data-ttu-id="951b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951b8-114">-DefaultProfile</span></span>
<span data-ttu-id="951b8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="951b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="951b8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="951b8-116">-Name</span></span>
<span data-ttu-id="951b8-117">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="951b8-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="951b8-118">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="951b8-118">Default to the location name.</span></span>

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

### <span data-ttu-id="951b8-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="951b8-119">-PassThru</span></span>
<span data-ttu-id="951b8-120">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="951b8-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="951b8-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="951b8-121">-RegistryName</span></span>
<span data-ttu-id="951b8-122">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="951b8-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="951b8-123">-Çoğaltma</span><span class="sxs-lookup"><span data-stu-id="951b8-123">-Replication</span></span>
<span data-ttu-id="951b8-124">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="951b8-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="951b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="951b8-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="951b8-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="951b8-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="951b8-127">-ResourceId</span></span>
<span data-ttu-id="951b8-128">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="951b8-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="951b8-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="951b8-129">-Confirm</span></span>
<span data-ttu-id="951b8-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="951b8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951b8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951b8-131">-WhatIf</span></span>
<span data-ttu-id="951b8-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="951b8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="951b8-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="951b8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951b8-134">CommonParameters</span></span>
<span data-ttu-id="951b8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="951b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951b8-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="951b8-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951b8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="951b8-137">INPUTS</span></span>

### <span data-ttu-id="951b8-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="951b8-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="951b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="951b8-139">System.String</span></span>

## <span data-ttu-id="951b8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="951b8-140">OUTPUTS</span></span>

### <span data-ttu-id="951b8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="951b8-141">System.Boolean</span></span>

## <span data-ttu-id="951b8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="951b8-142">NOTES</span></span>

## <span data-ttu-id="951b8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="951b8-143">RELATED LINKS</span></span>

[<span data-ttu-id="951b8-144">Yeni-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="951b8-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="951b8-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="951b8-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

