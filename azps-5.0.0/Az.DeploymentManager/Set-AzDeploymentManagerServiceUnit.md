---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320085"
---
# <span data-ttu-id="82515-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="82515-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="82515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82515-102">SYNOPSIS</span></span>
<span data-ttu-id="82515-103">Hizmet birimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="82515-103">Updates the service unit.</span></span>

## <span data-ttu-id="82515-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82515-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82515-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82515-105">DESCRIPTION</span></span>
<span data-ttu-id="82515-106">**Set-AzDeploymentManagerServiceUnit** cmdlet 'i belirtilen hizmet birimi nesnesini içeren bir hizmet birimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="82515-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="82515-107">Cmdlet, güncelleştirilmiş hizmet birimi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="82515-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="82515-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82515-108">EXAMPLES</span></span>

### <span data-ttu-id="82515-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="82515-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="82515-110">Bu komut, adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="82515-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="82515-111">Komut, güncelleştirilmiş hizmet birimi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="82515-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="82515-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82515-112">PARAMETERS</span></span>

### <span data-ttu-id="82515-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82515-113">-DefaultProfile</span></span>
<span data-ttu-id="82515-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82515-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82515-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82515-115">-InputObject</span></span>
<span data-ttu-id="82515-116">Hizmet birimi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="82515-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82515-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="82515-117">-Confirm</span></span>
<span data-ttu-id="82515-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82515-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82515-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82515-119">-WhatIf</span></span>
<span data-ttu-id="82515-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82515-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82515-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82515-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82515-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82515-122">CommonParameters</span></span>
<span data-ttu-id="82515-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82515-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82515-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="82515-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82515-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82515-125">INPUTS</span></span>

### <span data-ttu-id="82515-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="82515-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="82515-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82515-127">OUTPUTS</span></span>

### <span data-ttu-id="82515-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="82515-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="82515-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82515-129">NOTES</span></span>

## <span data-ttu-id="82515-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82515-130">RELATED LINKS</span></span>
