---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587996"
---
# <span data-ttu-id="fefe1-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fefe1-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="fefe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fefe1-102">SYNOPSIS</span></span>
<span data-ttu-id="fefe1-103">Kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fefe1-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fefe1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fefe1-104">SYNTAX</span></span>

### <span data-ttu-id="fefe1-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fefe1-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fefe1-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fefe1-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fefe1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fefe1-107">DESCRIPTION</span></span>
<span data-ttu-id="fefe1-108">**Remove-AzureRmContainerRegistry** cmdlet 'i kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fefe1-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="fefe1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fefe1-109">EXAMPLES</span></span>

### <span data-ttu-id="fefe1-110">Örnek 1: belirtilen kapsayıcı kayıt defterini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fefe1-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="fefe1-111">Bu komut belirtilen kapsayıcı kayıt defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fefe1-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="fefe1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fefe1-112">PARAMETERS</span></span>

### <span data-ttu-id="fefe1-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="fefe1-113">-Name</span></span>
<span data-ttu-id="fefe1-114">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="fefe1-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="fefe1-115">-Registry</span><span class="sxs-lookup"><span data-stu-id="fefe1-115">-Registry</span></span>
<span data-ttu-id="fefe1-116">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fefe1-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fefe1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fefe1-117">-ResourceGroupName</span></span>
<span data-ttu-id="fefe1-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fefe1-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="fefe1-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="fefe1-119">-Confirm</span></span>
<span data-ttu-id="fefe1-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fefe1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fefe1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fefe1-121">-WhatIf</span></span>
<span data-ttu-id="fefe1-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fefe1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fefe1-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fefe1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fefe1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefe1-124">-DefaultProfile</span></span>
<span data-ttu-id="fefe1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fefe1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fefe1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefe1-126">CommonParameters</span></span>
<span data-ttu-id="fefe1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fefe1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefe1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fefe1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefe1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fefe1-129">INPUTS</span></span>

### <span data-ttu-id="fefe1-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fefe1-130">PSContainerRegistry</span></span>
<span data-ttu-id="fefe1-131">Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fefe1-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="fefe1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fefe1-132">OUTPUTS</span></span>

### <span data-ttu-id="fefe1-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fefe1-133">None</span></span>

## <span data-ttu-id="fefe1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fefe1-134">NOTES</span></span>

## <span data-ttu-id="fefe1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fefe1-135">RELATED LINKS</span></span>

[<span data-ttu-id="fefe1-136">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fefe1-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="fefe1-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fefe1-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="fefe1-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fefe1-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

