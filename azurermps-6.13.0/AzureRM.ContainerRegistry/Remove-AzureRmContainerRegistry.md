---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763876"
---
# <span data-ttu-id="c138d-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c138d-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="c138d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c138d-102">SYNOPSIS</span></span>
<span data-ttu-id="c138d-103">Kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c138d-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c138d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c138d-104">SYNTAX</span></span>

### <span data-ttu-id="c138d-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c138d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c138d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c138d-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c138d-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c138d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c138d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c138d-108">DESCRIPTION</span></span>
<span data-ttu-id="c138d-109">Remove-AzureRmContainerRegistry cmdlet 'i kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c138d-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="c138d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c138d-110">EXAMPLES</span></span>

### <span data-ttu-id="c138d-111">Örnek 1: belirtilen kapsayıcı kayıt defterini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c138d-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="c138d-112">Bu komut belirtilen kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c138d-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="c138d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c138d-113">PARAMETERS</span></span>

### <span data-ttu-id="c138d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c138d-114">-DefaultProfile</span></span>
<span data-ttu-id="c138d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c138d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c138d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c138d-116">-Name</span></span>
<span data-ttu-id="c138d-117">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="c138d-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="c138d-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c138d-118">-PassThru</span></span>
<span data-ttu-id="c138d-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c138d-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="c138d-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="c138d-120">-Registry</span></span>
<span data-ttu-id="c138d-121">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c138d-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="c138d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c138d-122">-ResourceGroupName</span></span>
<span data-ttu-id="c138d-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c138d-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c138d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c138d-124">-ResourceId</span></span>
<span data-ttu-id="c138d-125">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c138d-125">The container registry resource id</span></span>

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

### <span data-ttu-id="c138d-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c138d-126">-Confirm</span></span>
<span data-ttu-id="c138d-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c138d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c138d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c138d-128">-WhatIf</span></span>
<span data-ttu-id="c138d-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c138d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c138d-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c138d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c138d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c138d-131">CommonParameters</span></span>
<span data-ttu-id="c138d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c138d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c138d-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c138d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c138d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c138d-134">INPUTS</span></span>

### <span data-ttu-id="c138d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c138d-135">System.String</span></span>

## <span data-ttu-id="c138d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c138d-136">OUTPUTS</span></span>

### <span data-ttu-id="c138d-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c138d-137">System.Boolean</span></span>

## <span data-ttu-id="c138d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c138d-138">NOTES</span></span>

## <span data-ttu-id="c138d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c138d-139">RELATED LINKS</span></span>

[<span data-ttu-id="c138d-140">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c138d-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="c138d-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c138d-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="c138d-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c138d-142">Update-AzureRmContainerRegistry</span></span>]()

