---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: c389f62f6f9b76f0ebdab30ddf600d333263a87c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752599"
---
# <span data-ttu-id="994aa-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="994aa-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="994aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994aa-102">SYNOPSIS</span></span>
<span data-ttu-id="994aa-103">Kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="994aa-103">Removes a container registry.</span></span>

## <span data-ttu-id="994aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="994aa-104">SYNTAX</span></span>

### <span data-ttu-id="994aa-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="994aa-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="994aa-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="994aa-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="994aa-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="994aa-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="994aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="994aa-108">DESCRIPTION</span></span>
<span data-ttu-id="994aa-109">Remove-AzContainerRegistry cmdlet 'i kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="994aa-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="994aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="994aa-110">EXAMPLES</span></span>

### <span data-ttu-id="994aa-111">Örnek 1: belirtilen kapsayıcı kayıt defterini kaldırma</span><span class="sxs-lookup"><span data-stu-id="994aa-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="994aa-112">Bu komut belirtilen kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="994aa-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="994aa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="994aa-113">PARAMETERS</span></span>

### <span data-ttu-id="994aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994aa-114">-DefaultProfile</span></span>
<span data-ttu-id="994aa-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="994aa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="994aa-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="994aa-116">-Name</span></span>
<span data-ttu-id="994aa-117">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="994aa-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="994aa-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="994aa-118">-PassThru</span></span>
<span data-ttu-id="994aa-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="994aa-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="994aa-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="994aa-120">-Registry</span></span>
<span data-ttu-id="994aa-121">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="994aa-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="994aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="994aa-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="994aa-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="994aa-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="994aa-124">-ResourceId</span></span>
<span data-ttu-id="994aa-125">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="994aa-125">The container registry resource id</span></span>

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

### <span data-ttu-id="994aa-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="994aa-126">-Confirm</span></span>
<span data-ttu-id="994aa-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="994aa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="994aa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994aa-128">-WhatIf</span></span>
<span data-ttu-id="994aa-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="994aa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="994aa-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="994aa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="994aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994aa-131">CommonParameters</span></span>
<span data-ttu-id="994aa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="994aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994aa-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="994aa-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994aa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="994aa-134">INPUTS</span></span>

### <span data-ttu-id="994aa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="994aa-135">System.String</span></span>

## <span data-ttu-id="994aa-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="994aa-136">OUTPUTS</span></span>

### <span data-ttu-id="994aa-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="994aa-137">System.Boolean</span></span>

## <span data-ttu-id="994aa-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="994aa-138">NOTES</span></span>

## <span data-ttu-id="994aa-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="994aa-139">RELATED LINKS</span></span>

[<span data-ttu-id="994aa-140">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="994aa-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="994aa-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="994aa-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="994aa-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="994aa-142">Update-AzContainerRegistry</span></span>]()

