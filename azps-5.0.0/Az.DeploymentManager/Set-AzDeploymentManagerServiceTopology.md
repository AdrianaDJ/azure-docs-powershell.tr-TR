---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320086"
---
# <span data-ttu-id="6964f-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6964f-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="6964f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6964f-102">SYNOPSIS</span></span>
<span data-ttu-id="6964f-103">Hizmet topolojisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6964f-103">Updates the service topology.</span></span>

## <span data-ttu-id="6964f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6964f-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6964f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6964f-105">DESCRIPTION</span></span>
<span data-ttu-id="6964f-106">**Set-AzDeploymentManagerServiceTopology** cmdlet 'i belirtilen hizmet topolojisi nesnesiyle bir hizmet topolojisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6964f-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="6964f-107">Cmdlet, güncelleştirilmiş hizmet topolojisi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6964f-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="6964f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6964f-108">EXAMPLES</span></span>

### <span data-ttu-id="6964f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6964f-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="6964f-110">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6964f-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="6964f-111">Komut, güncelleştirilmiş hizmet topolojisi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6964f-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="6964f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6964f-112">PARAMETERS</span></span>

### <span data-ttu-id="6964f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6964f-113">-DefaultProfile</span></span>
<span data-ttu-id="6964f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6964f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6964f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6964f-115">-InputObject</span></span>
<span data-ttu-id="6964f-116">Hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6964f-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6964f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="6964f-117">-Confirm</span></span>
<span data-ttu-id="6964f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6964f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6964f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6964f-119">-WhatIf</span></span>
<span data-ttu-id="6964f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6964f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6964f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6964f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6964f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6964f-122">CommonParameters</span></span>
<span data-ttu-id="6964f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6964f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6964f-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6964f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6964f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6964f-125">INPUTS</span></span>

### <span data-ttu-id="6964f-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="6964f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="6964f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6964f-127">OUTPUTS</span></span>

### <span data-ttu-id="6964f-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="6964f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="6964f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6964f-129">NOTES</span></span>

## <span data-ttu-id="6964f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6964f-130">RELATED LINKS</span></span>
