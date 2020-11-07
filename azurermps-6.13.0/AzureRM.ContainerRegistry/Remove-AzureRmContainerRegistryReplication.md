---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763875"
---
# <span data-ttu-id="4306e-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4306e-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="4306e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4306e-102">SYNOPSIS</span></span>
<span data-ttu-id="4306e-103">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4306e-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4306e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4306e-104">SYNTAX</span></span>

### <span data-ttu-id="4306e-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4306e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4306e-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4306e-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4306e-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4306e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4306e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4306e-108">DESCRIPTION</span></span>
<span data-ttu-id="4306e-109">Remove-AzureRmContainerRegistryReplication cmdlet 'i kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4306e-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="4306e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4306e-110">EXAMPLES</span></span>

### <span data-ttu-id="4306e-111">Örnek 1: kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4306e-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="4306e-112">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4306e-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="4306e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4306e-113">PARAMETERS</span></span>

### <span data-ttu-id="4306e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4306e-114">-DefaultProfile</span></span>
<span data-ttu-id="4306e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4306e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4306e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4306e-116">-Name</span></span>
<span data-ttu-id="4306e-117">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="4306e-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="4306e-118">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="4306e-118">Default to the location name.</span></span>

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

### <span data-ttu-id="4306e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4306e-119">-PassThru</span></span>
<span data-ttu-id="4306e-120">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4306e-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="4306e-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4306e-121">-RegistryName</span></span>
<span data-ttu-id="4306e-122">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="4306e-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="4306e-123">-Replicatoın</span><span class="sxs-lookup"><span data-stu-id="4306e-123">-Replicatoin</span></span>
<span data-ttu-id="4306e-124">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4306e-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4306e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4306e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4306e-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4306e-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="4306e-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4306e-127">-ResourceId</span></span>
<span data-ttu-id="4306e-128">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4306e-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="4306e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="4306e-129">-Confirm</span></span>
<span data-ttu-id="4306e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4306e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4306e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4306e-131">-WhatIf</span></span>
<span data-ttu-id="4306e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4306e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4306e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4306e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4306e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4306e-134">CommonParameters</span></span>
<span data-ttu-id="4306e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4306e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4306e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4306e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4306e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4306e-137">INPUTS</span></span>

### <span data-ttu-id="4306e-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4306e-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="4306e-139">Parametreler: Replicatoın (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4306e-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="4306e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4306e-140">System.String</span></span>

## <span data-ttu-id="4306e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4306e-141">OUTPUTS</span></span>

### <span data-ttu-id="4306e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4306e-142">System.Boolean</span></span>

## <span data-ttu-id="4306e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4306e-143">NOTES</span></span>

## <span data-ttu-id="4306e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4306e-144">RELATED LINKS</span></span>

[<span data-ttu-id="4306e-145">Yeni-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4306e-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="4306e-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4306e-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

