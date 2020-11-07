---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: dee0e1f4dab19af5de4d7f8ce7a9fe10b8f51d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761178"
---
# <span data-ttu-id="de19e-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de19e-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="de19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de19e-102">SYNOPSIS</span></span>
<span data-ttu-id="de19e-103">Kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="de19e-103">Removes a container registry.</span></span>

## <span data-ttu-id="de19e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de19e-104">SYNTAX</span></span>

### <span data-ttu-id="de19e-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="de19e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de19e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de19e-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de19e-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="de19e-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de19e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="de19e-108">DESCRIPTION</span></span>
<span data-ttu-id="de19e-109">Remove-AzContainerRegistry cmdlet 'i kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="de19e-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="de19e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de19e-110">EXAMPLES</span></span>

### <span data-ttu-id="de19e-111">Örnek 1: belirtilen kapsayıcı kayıt defterini kaldırma</span><span class="sxs-lookup"><span data-stu-id="de19e-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="de19e-112">Bu komut belirtilen kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="de19e-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="de19e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de19e-113">PARAMETERS</span></span>

### <span data-ttu-id="de19e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de19e-114">-DefaultProfile</span></span>
<span data-ttu-id="de19e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="de19e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de19e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="de19e-116">-Name</span></span>
<span data-ttu-id="de19e-117">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="de19e-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="de19e-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="de19e-118">-PassThru</span></span>
<span data-ttu-id="de19e-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="de19e-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="de19e-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="de19e-120">-Registry</span></span>
<span data-ttu-id="de19e-121">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="de19e-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="de19e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de19e-122">-ResourceGroupName</span></span>
<span data-ttu-id="de19e-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="de19e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="de19e-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="de19e-124">-ResourceId</span></span>
<span data-ttu-id="de19e-125">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="de19e-125">The container registry resource id</span></span>

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

### <span data-ttu-id="de19e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="de19e-126">-Confirm</span></span>
<span data-ttu-id="de19e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de19e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de19e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de19e-128">-WhatIf</span></span>
<span data-ttu-id="de19e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de19e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de19e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de19e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de19e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de19e-131">CommonParameters</span></span>
<span data-ttu-id="de19e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de19e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de19e-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de19e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de19e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de19e-134">INPUTS</span></span>

### <span data-ttu-id="de19e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="de19e-135">System.String</span></span>

## <span data-ttu-id="de19e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de19e-136">OUTPUTS</span></span>

### <span data-ttu-id="de19e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de19e-137">System.Boolean</span></span>

## <span data-ttu-id="de19e-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de19e-138">NOTES</span></span>

## <span data-ttu-id="de19e-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de19e-139">RELATED LINKS</span></span>

[<span data-ttu-id="de19e-140">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de19e-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="de19e-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de19e-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="de19e-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de19e-142">Update-AzContainerRegistry</span></span>]()
