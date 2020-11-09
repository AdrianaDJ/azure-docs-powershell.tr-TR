---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319633"
---
# <span data-ttu-id="40cea-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-101">Update-AzContainerService</span></span>

## <span data-ttu-id="40cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40cea-102">SYNOPSIS</span></span>
<span data-ttu-id="40cea-103">Kapsayıcı hizmetin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40cea-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="40cea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40cea-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40cea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40cea-105">DESCRIPTION</span></span>
<span data-ttu-id="40cea-106">**Update-AzContainerService** cmdlet 'i, bir kapsayıcı hizmetinin durumunu hizmetin yerel örneğiyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40cea-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="40cea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40cea-107">EXAMPLES</span></span>

### <span data-ttu-id="40cea-108">Örnek 1: kapsayıcı hizmeti güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="40cea-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="40cea-109">Bu komut, Get-AzContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="40cea-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="40cea-110">Komut, ardışık düzen işlecini kullanarak bu nesneyi Remove-AzContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="40cea-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="40cea-111">**Remove-AzContainerServiceAgentPoolProfile** , AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="40cea-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="40cea-112">Komut sonucu Add-AzContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="40cea-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="40cea-113">**Add-AzContainerServiceAgentPoolProfile** , AgentPool01 adında bir profil ekler ve belirtilen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="40cea-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="40cea-114">Komut sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="40cea-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="40cea-115">Geçerli cmdlet, kapsayıcı hizmetini Bu komutta yapılan değişiklikleri yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40cea-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="40cea-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40cea-116">PARAMETERS</span></span>

### <span data-ttu-id="40cea-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="40cea-117">-AsJob</span></span>
<span data-ttu-id="40cea-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="40cea-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40cea-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-119">-ContainerService</span></span>
<span data-ttu-id="40cea-120">Değişiklikleri içeren bir yerel **kapsayıcı hizmet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40cea-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40cea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cea-121">-DefaultProfile</span></span>
<span data-ttu-id="40cea-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40cea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40cea-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="40cea-123">-Name</span></span>
<span data-ttu-id="40cea-124">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40cea-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cea-125">-ResourceGroupName</span></span>
<span data-ttu-id="40cea-126">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="40cea-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cea-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="40cea-127">-Confirm</span></span>
<span data-ttu-id="40cea-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40cea-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40cea-129">-WhatIf</span></span>
<span data-ttu-id="40cea-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40cea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40cea-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40cea-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cea-132">CommonParameters</span></span>
<span data-ttu-id="40cea-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40cea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cea-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40cea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cea-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40cea-135">INPUTS</span></span>

### <span data-ttu-id="40cea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="40cea-136">System.String</span></span>

### <span data-ttu-id="40cea-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="40cea-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40cea-138">OUTPUTS</span></span>

### <span data-ttu-id="40cea-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="40cea-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40cea-140">NOTES</span></span>

## <span data-ttu-id="40cea-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40cea-141">RELATED LINKS</span></span>

[<span data-ttu-id="40cea-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="40cea-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="40cea-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="40cea-144">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="40cea-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40cea-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="40cea-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="40cea-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


