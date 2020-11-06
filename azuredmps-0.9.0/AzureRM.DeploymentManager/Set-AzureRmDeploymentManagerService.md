---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571389"
---
# <span data-ttu-id="eb45c-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="eb45c-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="eb45c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb45c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb45c-103">Hizmet topolojisinde bir hizmeti güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eb45c-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="eb45c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb45c-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb45c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb45c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb45c-106">**Set-AzureRmDeploymentManagerService** cmdlet 'i belirtilen hizmet nesnesiyle bir hizmeti güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eb45c-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="eb45c-107">Cmdlet, güncelleştirilmiş hizmet nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb45c-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="eb45c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb45c-108">EXAMPLES</span></span>

### <span data-ttu-id="eb45c-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eb45c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="eb45c-110">Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eb45c-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="eb45c-111">Hizmet, $serviceObject belirlenen özelliklere güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="eb45c-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="eb45c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb45c-112">PARAMETERS</span></span>

### <span data-ttu-id="eb45c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb45c-113">-DefaultProfile</span></span>
<span data-ttu-id="eb45c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb45c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb45c-115">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="eb45c-115">-Service</span></span>
<span data-ttu-id="eb45c-116">Hizmet nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eb45c-116">The service object.</span></span>

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

### <span data-ttu-id="eb45c-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb45c-117">-Confirm</span></span>
<span data-ttu-id="eb45c-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb45c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb45c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb45c-119">-WhatIf</span></span>
<span data-ttu-id="eb45c-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb45c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb45c-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb45c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb45c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb45c-122">CommonParameters</span></span>
<span data-ttu-id="eb45c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb45c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb45c-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb45c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb45c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb45c-125">INPUTS</span></span>

### <span data-ttu-id="eb45c-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="eb45c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="eb45c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb45c-127">OUTPUTS</span></span>

### <span data-ttu-id="eb45c-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="eb45c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="eb45c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb45c-129">NOTES</span></span>

## <span data-ttu-id="eb45c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb45c-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb45c-131">Yeni-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="eb45c-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="eb45c-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="eb45c-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="eb45c-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="eb45c-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)