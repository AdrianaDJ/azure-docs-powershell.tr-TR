---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591032"
---
# <span data-ttu-id="f0c4a-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0c4a-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="f0c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c4a-103">Kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0c4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0c4a-104">SYNTAX</span></span>

### <span data-ttu-id="f0c4a-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0c4a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c4a-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c4a-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c4a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f0c4a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0c4a-108">DESCRIPTION</span></span>
<span data-ttu-id="f0c4a-109">Remove-AzureRmContainerRegistry cmdlet 'i kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="f0c4a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0c4a-110">EXAMPLES</span></span>

### <span data-ttu-id="f0c4a-111">Örnek 1: belirtilen kapsayıcı kayıt defterini kaldırma</span><span class="sxs-lookup"><span data-stu-id="f0c4a-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="f0c4a-112">Bu komut belirtilen kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="f0c4a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0c4a-113">PARAMETERS</span></span>

### <span data-ttu-id="f0c4a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0c4a-114">-Name</span></span>
<span data-ttu-id="f0c4a-115">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="f0c4a-116">-Registry</span></span>
<span data-ttu-id="f0c4a-117">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-117">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c4a-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0c4a-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0c4a-120">-Confirm</span></span>
<span data-ttu-id="f0c4a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c4a-122">-WhatIf</span></span>
<span data-ttu-id="f0c4a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c4a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c4a-125">-DefaultProfile</span></span>
<span data-ttu-id="f0c4a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f0c4a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0c4a-127">-ResourceId</span></span>
<span data-ttu-id="f0c4a-128">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f0c4a-128">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f0c4a-129">-PassThru</span></span>
<span data-ttu-id="f0c4a-130">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c4a-131">CommonParameters</span></span>
<span data-ttu-id="f0c4a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0c4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c4a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c4a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c4a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0c4a-134">INPUTS</span></span>

### <span data-ttu-id="f0c4a-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0c4a-135">PSContainerRegistry</span></span>
<span data-ttu-id="f0c4a-136">Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f0c4a-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="f0c4a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0c4a-137">OUTPUTS</span></span>

### <span data-ttu-id="f0c4a-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f0c4a-138">None</span></span>

## <span data-ttu-id="f0c4a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0c4a-139">NOTES</span></span>

## <span data-ttu-id="f0c4a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0c4a-140">RELATED LINKS</span></span>

[<span data-ttu-id="f0c4a-141">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0c4a-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="f0c4a-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0c4a-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="f0c4a-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0c4a-143">Update-AzureRmContainerRegistry</span></span>]()

