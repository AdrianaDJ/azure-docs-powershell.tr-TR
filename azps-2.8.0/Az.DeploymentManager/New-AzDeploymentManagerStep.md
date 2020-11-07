---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752132"
---
# <span data-ttu-id="e9d35-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="e9d35-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="e9d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d35-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d35-103">Adım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9d35-103">Creates a step.</span></span>

## <span data-ttu-id="e9d35-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9d35-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9d35-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9d35-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d35-106">**New-AzDeploymentManagerStep** cmdlet 'i, rollouts 'de başvurulabilen bir dağıtım adımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9d35-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="e9d35-107">*Name* , *resourcegroupname* ve gerekli özellikleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="e9d35-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="e9d35-108">Döndürülen nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerStep cmdlet 'ini kullanarak değişiklikleri adıma uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9d35-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="e9d35-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9d35-109">EXAMPLES</span></span>

### <span data-ttu-id="e9d35-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9d35-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="e9d35-111">ContosoService1WaitStep adını, kaynağın konumu olarak merkezi olan ContosoResourceGroup ile bir adım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9d35-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="e9d35-112">Duration özelliği, sonraki adımı çalıştırmadan önce tüm işlemin bekleyeceği süreyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e9d35-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="e9d35-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9d35-113">PARAMETERS</span></span>

### <span data-ttu-id="e9d35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d35-114">-DefaultProfile</span></span>
<span data-ttu-id="e9d35-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9d35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d35-116">-Süre</span><span class="sxs-lookup"><span data-stu-id="e9d35-116">-Duration</span></span>
<span data-ttu-id="e9d35-117">ISO 8601 biçiminde bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="e9d35-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="e9d35-118">Örneğin: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="e9d35-118">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d35-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="e9d35-119">-Location</span></span>
<span data-ttu-id="e9d35-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e9d35-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d35-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9d35-121">-Name</span></span>
<span data-ttu-id="e9d35-122">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="e9d35-122">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d35-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9d35-124">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e9d35-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d35-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e9d35-125">-Tag</span></span>
<span data-ttu-id="e9d35-126">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="e9d35-126">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e9d35-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9d35-127">-Confirm</span></span>
<span data-ttu-id="e9d35-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9d35-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9d35-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d35-129">-WhatIf</span></span>
<span data-ttu-id="e9d35-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9d35-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9d35-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9d35-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9d35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d35-132">CommonParameters</span></span>
<span data-ttu-id="e9d35-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9d35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d35-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d35-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d35-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9d35-135">INPUTS</span></span>

### <span data-ttu-id="e9d35-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9d35-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9d35-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9d35-137">OUTPUTS</span></span>

### <span data-ttu-id="e9d35-138">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="e9d35-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="e9d35-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9d35-139">NOTES</span></span>

## <span data-ttu-id="e9d35-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9d35-140">RELATED LINKS</span></span>
