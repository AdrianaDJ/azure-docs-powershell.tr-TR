---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/new-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/New-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/New-AzureRmDevSpacesController.md
ms.openlocfilehash: 13fea6a0f7c7fda06e171538c92fe52db969fe36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762950"
---
# <span data-ttu-id="889de-101">New-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="889de-101">New-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="889de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="889de-102">SYNOPSIS</span></span>
<span data-ttu-id="889de-103">Yeni bir Azure DevSpaces denetleyicisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="889de-103">Create a new Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="889de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="889de-104">SYNTAX</span></span>

```
New-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-TargetResourceGroupName] <String> [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="889de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="889de-105">DESCRIPTION</span></span>
<span data-ttu-id="889de-106">Yeni bir Azure DevSpaces denetleyicisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="889de-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="889de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="889de-107">EXAMPLES</span></span>

### <span data-ttu-id="889de-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="889de-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="889de-109">Bir ad devSpaceName ile resourcegroup devSpaceResourceGroup 'de bir DevSpaces denetleyicisi oluştur.</span><span class="sxs-lookup"><span data-stu-id="889de-109">Crreate a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="889de-110">Bu denetleyicinin hedef olarak clusterName kümesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="889de-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="889de-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="889de-111">PARAMETERS</span></span>

### <span data-ttu-id="889de-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="889de-112">-AsJob</span></span>
<span data-ttu-id="889de-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="889de-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="889de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889de-114">-DefaultProfile</span></span>
<span data-ttu-id="889de-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="889de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="889de-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="889de-116">-Name</span></span>
<span data-ttu-id="889de-117">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="889de-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889de-118">-ResourceGroupName</span></span>
<span data-ttu-id="889de-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="889de-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889de-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="889de-120">-Tag</span></span>
<span data-ttu-id="889de-121">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="889de-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889de-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="889de-122">-TargetClusterName</span></span>
<span data-ttu-id="889de-123">Hedef küme adı.</span><span class="sxs-lookup"><span data-stu-id="889de-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889de-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889de-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="889de-125">Hedef kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="889de-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889de-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="889de-126">-Confirm</span></span>
<span data-ttu-id="889de-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="889de-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="889de-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="889de-128">-WhatIf</span></span>
<span data-ttu-id="889de-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="889de-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="889de-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="889de-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="889de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889de-131">CommonParameters</span></span>
<span data-ttu-id="889de-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="889de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889de-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="889de-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889de-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="889de-134">INPUTS</span></span>

### <span data-ttu-id="889de-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="889de-135">None</span></span>

## <span data-ttu-id="889de-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="889de-136">OUTPUTS</span></span>

### <span data-ttu-id="889de-137">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="889de-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="889de-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="889de-138">NOTES</span></span>

## <span data-ttu-id="889de-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="889de-139">RELATED LINKS</span></span>
