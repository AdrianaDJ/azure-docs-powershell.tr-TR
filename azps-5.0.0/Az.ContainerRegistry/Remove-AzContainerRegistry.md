---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275579"
---
# <span data-ttu-id="90c12-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90c12-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="90c12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c12-102">SYNOPSIS</span></span>
<span data-ttu-id="90c12-103">Kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="90c12-103">Removes a container registry.</span></span>

## <span data-ttu-id="90c12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90c12-104">SYNTAX</span></span>

### <span data-ttu-id="90c12-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90c12-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c12-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90c12-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c12-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="90c12-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c12-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="90c12-108">DESCRIPTION</span></span>
<span data-ttu-id="90c12-109">Remove-AzContainerRegistry cmdlet 'i kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="90c12-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="90c12-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90c12-110">EXAMPLES</span></span>

### <span data-ttu-id="90c12-111">Örnek 1: belirtilen kapsayıcı kayıt defterini kaldırma</span><span class="sxs-lookup"><span data-stu-id="90c12-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="90c12-112">Bu komut belirtilen kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="90c12-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="90c12-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90c12-113">PARAMETERS</span></span>

### <span data-ttu-id="90c12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c12-114">-DefaultProfile</span></span>
<span data-ttu-id="90c12-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="90c12-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90c12-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="90c12-116">-Name</span></span>
<span data-ttu-id="90c12-117">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="90c12-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c12-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="90c12-118">-PassThru</span></span>
<span data-ttu-id="90c12-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="90c12-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="90c12-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="90c12-120">-Registry</span></span>
<span data-ttu-id="90c12-121">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="90c12-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c12-122">-ResourceGroupName</span></span>
<span data-ttu-id="90c12-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="90c12-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c12-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="90c12-124">-ResourceId</span></span>
<span data-ttu-id="90c12-125">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="90c12-125">The container registry resource id</span></span>

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

### <span data-ttu-id="90c12-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="90c12-126">-Confirm</span></span>
<span data-ttu-id="90c12-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90c12-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c12-128">-WhatIf</span></span>
<span data-ttu-id="90c12-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90c12-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c12-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90c12-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c12-131">CommonParameters</span></span>
<span data-ttu-id="90c12-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90c12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c12-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90c12-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c12-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90c12-134">INPUTS</span></span>

### <span data-ttu-id="90c12-135">System. String</span><span class="sxs-lookup"><span data-stu-id="90c12-135">System.String</span></span>

## <span data-ttu-id="90c12-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90c12-136">OUTPUTS</span></span>

### <span data-ttu-id="90c12-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90c12-137">System.Boolean</span></span>

## <span data-ttu-id="90c12-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90c12-138">NOTES</span></span>

## <span data-ttu-id="90c12-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90c12-139">RELATED LINKS</span></span>

[<span data-ttu-id="90c12-140">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90c12-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="90c12-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90c12-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="90c12-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90c12-142">Update-AzContainerRegistry</span></span>]()

