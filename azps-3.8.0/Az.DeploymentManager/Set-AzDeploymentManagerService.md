---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104364"
---
# <span data-ttu-id="2db59-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="2db59-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="2db59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db59-102">SYNOPSIS</span></span>
<span data-ttu-id="2db59-103">Hizmeti güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db59-103">Updates the service.</span></span>

## <span data-ttu-id="2db59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2db59-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2db59-105">DESCRIPTION</span></span>
<span data-ttu-id="2db59-106">**Set-AzDeploymentManagerService** cmdlet 'i belirtilen hizmet nesnesiyle bir hizmeti güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db59-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="2db59-107">Cmdlet, güncelleştirilmiş hizmet nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2db59-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="2db59-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2db59-108">EXAMPLES</span></span>

### <span data-ttu-id="2db59-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2db59-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="2db59-110">Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2db59-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="2db59-111">Hizmet, $serviceObject belirlenen özelliklere güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="2db59-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="2db59-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2db59-112">PARAMETERS</span></span>

### <span data-ttu-id="2db59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db59-113">-DefaultProfile</span></span>
<span data-ttu-id="2db59-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2db59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db59-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db59-115">-InputObject</span></span>
<span data-ttu-id="2db59-116">Hizmet nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2db59-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db59-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="2db59-117">-Confirm</span></span>
<span data-ttu-id="2db59-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2db59-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db59-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db59-119">-WhatIf</span></span>
<span data-ttu-id="2db59-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db59-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db59-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2db59-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db59-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db59-122">CommonParameters</span></span>
<span data-ttu-id="2db59-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2db59-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db59-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2db59-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db59-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2db59-125">INPUTS</span></span>

### <span data-ttu-id="2db59-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="2db59-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="2db59-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2db59-127">OUTPUTS</span></span>

### <span data-ttu-id="2db59-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="2db59-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="2db59-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2db59-129">NOTES</span></span>

## <span data-ttu-id="2db59-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2db59-130">RELATED LINKS</span></span>
