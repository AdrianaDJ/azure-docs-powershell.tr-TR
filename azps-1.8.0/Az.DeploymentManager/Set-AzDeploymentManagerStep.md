---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 15944b324cc2b33d3186d7c84da16c72351dcc99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760967"
---
# <span data-ttu-id="b2b3b-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b2b3b-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="b2b3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b3b-103">Adımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-103">Updates the step.</span></span>

## <span data-ttu-id="b2b3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2b3b-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b3b-106">**Set-AzDeploymentManagerStep** cmdlet 'i belirtilen adım nesnesiyle bir adımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="b2b3b-107">Cmdlet, güncelleştirilmiş adım nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="b2b3b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2b3b-108">EXAMPLES</span></span>

### <span data-ttu-id="b2b3b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2b3b-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="b2b3b-110">Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleştiğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="b2b3b-111">Adım $stepObject belirlenen özelliklere güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="b2b3b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2b3b-112">PARAMETERS</span></span>

### <span data-ttu-id="b2b3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b3b-113">-DefaultProfile</span></span>
<span data-ttu-id="b2b3b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b3b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2b3b-115">-InputObject</span></span>
<span data-ttu-id="b2b3b-116">Adım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b3b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2b3b-117">-Confirm</span></span>
<span data-ttu-id="b2b3b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b3b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b3b-119">-WhatIf</span></span>
<span data-ttu-id="b2b3b-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b3b-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b3b-122">CommonParameters</span></span>
<span data-ttu-id="b2b3b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2b3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b3b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b3b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2b3b-125">INPUTS</span></span>

### <span data-ttu-id="b2b3b-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b2b3b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b2b3b-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2b3b-127">OUTPUTS</span></span>

### <span data-ttu-id="b2b3b-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b2b3b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b2b3b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2b3b-129">NOTES</span></span>

## <span data-ttu-id="b2b3b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2b3b-130">RELATED LINKS</span></span>