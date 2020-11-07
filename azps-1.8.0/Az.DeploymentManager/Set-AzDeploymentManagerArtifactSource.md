---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 32e5293f7c5bb62711a6510c590aa1ba7f4229b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760975"
---
# <span data-ttu-id="671ee-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="671ee-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="671ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="671ee-102">SYNOPSIS</span></span>
<span data-ttu-id="671ee-103">Yapılar kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="671ee-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="671ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="671ee-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="671ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="671ee-105">DESCRIPTION</span></span>
<span data-ttu-id="671ee-106">**Set-AzDeploymentManagerArtifactSource** cmdlet 'i, bir yapıt kaynağını belirtilen yapıt kaynağı nesnesiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="671ee-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="671ee-107">Cmdlet, güncelleştirilmiş ArtifactSource nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="671ee-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="671ee-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="671ee-108">EXAMPLES</span></span>

### <span data-ttu-id="671ee-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="671ee-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="671ee-110">Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="671ee-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="671ee-111">Yapıt kaynağı $artifactSourceObject belirlenen özelliklere güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="671ee-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="671ee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="671ee-112">PARAMETERS</span></span>

### <span data-ttu-id="671ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671ee-113">-DefaultProfile</span></span>
<span data-ttu-id="671ee-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="671ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="671ee-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="671ee-115">-InputObject</span></span>
<span data-ttu-id="671ee-116">Yapıt kaynağı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="671ee-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="671ee-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="671ee-117">-Confirm</span></span>
<span data-ttu-id="671ee-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="671ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="671ee-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="671ee-119">-WhatIf</span></span>
<span data-ttu-id="671ee-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="671ee-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="671ee-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="671ee-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="671ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671ee-122">CommonParameters</span></span>
<span data-ttu-id="671ee-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="671ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671ee-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="671ee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="671ee-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="671ee-125">INPUTS</span></span>

### <span data-ttu-id="671ee-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="671ee-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="671ee-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="671ee-127">OUTPUTS</span></span>

### <span data-ttu-id="671ee-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="671ee-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="671ee-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="671ee-129">NOTES</span></span>

## <span data-ttu-id="671ee-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="671ee-130">RELATED LINKS</span></span>
