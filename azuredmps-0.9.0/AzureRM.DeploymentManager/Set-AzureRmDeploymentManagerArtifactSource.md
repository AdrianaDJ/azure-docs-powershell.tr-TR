---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571685"
---
# <span data-ttu-id="765ab-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="765ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="765ab-102">SYNOPSIS</span></span>
<span data-ttu-id="765ab-103">Yapıt kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="765ab-103">Updates an artifact source.</span></span>

## <span data-ttu-id="765ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="765ab-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="765ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="765ab-105">DESCRIPTION</span></span>
<span data-ttu-id="765ab-106">**Set-AzureRmDeploymentManagerArtifactSource** cmdlet 'i, bir yapıt kaynağını belirtilen yapıt kaynağı nesnesiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="765ab-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="765ab-107">Cmdlet, güncelleştirilmiş ArtifactSource nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="765ab-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="765ab-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="765ab-108">EXAMPLES</span></span>

### <span data-ttu-id="765ab-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="765ab-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="765ab-110">Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="765ab-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="765ab-111">Yapıt kaynağı $artifactSourceObject belirlenen özelliklere güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="765ab-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="765ab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="765ab-112">PARAMETERS</span></span>

### <span data-ttu-id="765ab-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-113">-ArtifactSource</span></span>
<span data-ttu-id="765ab-114">Yapıt kaynağı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="765ab-114">The artifact source object.</span></span>

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

### <span data-ttu-id="765ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765ab-115">-DefaultProfile</span></span>
<span data-ttu-id="765ab-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="765ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="765ab-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="765ab-117">-Confirm</span></span>
<span data-ttu-id="765ab-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="765ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="765ab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="765ab-119">-WhatIf</span></span>
<span data-ttu-id="765ab-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="765ab-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="765ab-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="765ab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="765ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765ab-122">CommonParameters</span></span>
<span data-ttu-id="765ab-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="765ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765ab-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="765ab-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765ab-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="765ab-125">INPUTS</span></span>

### <span data-ttu-id="765ab-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="765ab-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="765ab-127">OUTPUTS</span></span>

### <span data-ttu-id="765ab-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="765ab-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="765ab-129">NOTES</span></span>

## <span data-ttu-id="765ab-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="765ab-130">RELATED LINKS</span></span>

[<span data-ttu-id="765ab-131">Yeni-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="765ab-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="765ab-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="765ab-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)