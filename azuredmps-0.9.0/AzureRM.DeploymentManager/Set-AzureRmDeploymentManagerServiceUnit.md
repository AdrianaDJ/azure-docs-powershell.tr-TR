---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571858"
---
# <span data-ttu-id="f45a1-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f45a1-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="f45a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f45a1-103">Hizmet birimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f45a1-103">Updates a service unit.</span></span>

## <span data-ttu-id="f45a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f45a1-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f45a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f45a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f45a1-106">**Set-AzureRmDeploymentManagerServiceUnit** cmdlet 'i belirtilen hizmet birimi nesnesini içeren bir hizmet birimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f45a1-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="f45a1-107">Cmdlet, güncelleştirilmiş hizmet birimi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f45a1-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="f45a1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f45a1-108">EXAMPLES</span></span>

### <span data-ttu-id="f45a1-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f45a1-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="f45a1-110">Bu komut, adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f45a1-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="f45a1-111">Komut, güncelleştirilmiş hizmet birimi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f45a1-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="f45a1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f45a1-112">PARAMETERS</span></span>

### <span data-ttu-id="f45a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45a1-113">-DefaultProfile</span></span>
<span data-ttu-id="f45a1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f45a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45a1-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f45a1-115">-ServiceUnit</span></span>
<span data-ttu-id="f45a1-116">Hizmet birimi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f45a1-116">The service unit object.</span></span>

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

### <span data-ttu-id="f45a1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f45a1-117">-Confirm</span></span>
<span data-ttu-id="f45a1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f45a1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f45a1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f45a1-119">-WhatIf</span></span>
<span data-ttu-id="f45a1-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f45a1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f45a1-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f45a1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f45a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45a1-122">CommonParameters</span></span>
<span data-ttu-id="f45a1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f45a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45a1-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45a1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f45a1-125">INPUTS</span></span>

### <span data-ttu-id="f45a1-126">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="f45a1-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="f45a1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f45a1-127">OUTPUTS</span></span>

### <span data-ttu-id="f45a1-128">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="f45a1-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="f45a1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f45a1-129">NOTES</span></span>

## <span data-ttu-id="f45a1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f45a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="f45a1-131">Yeni-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f45a1-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="f45a1-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f45a1-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="f45a1-133">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="f45a1-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)