---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 086085bd1a36c1508cf489d224ddd6bff4651c50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761206"
---
# <span data-ttu-id="fc693-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-101">Update-AzContainerService</span></span>

## <span data-ttu-id="fc693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc693-102">SYNOPSIS</span></span>
<span data-ttu-id="fc693-103">Kapsayıcı hizmetin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc693-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="fc693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc693-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc693-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc693-105">DESCRIPTION</span></span>
<span data-ttu-id="fc693-106">**Update-AzContainerService** cmdlet 'i, bir kapsayıcı hizmetinin durumunu hizmetin yerel örneğiyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc693-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="fc693-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc693-107">EXAMPLES</span></span>

### <span data-ttu-id="fc693-108">Örnek 1: kapsayıcı hizmeti güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fc693-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="fc693-109">Bu komut, Get-AzContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="fc693-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="fc693-110">Komut, ardışık düzen işlecini kullanarak bu nesneyi Remove-AzContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fc693-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fc693-111">**Remove-AzContainerServiceAgentPoolProfile** , AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc693-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="fc693-112">Komut sonucu Add-AzContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fc693-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="fc693-113">**Add-AzContainerServiceAgentPoolProfile** , AgentPool01 adında bir profil ekler ve belirtilen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="fc693-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="fc693-114">Komut sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="fc693-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="fc693-115">Geçerli cmdlet, kapsayıcı hizmetini Bu komutta yapılan değişiklikleri yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc693-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="fc693-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc693-116">PARAMETERS</span></span>

### <span data-ttu-id="fc693-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="fc693-117">-AsJob</span></span>
<span data-ttu-id="fc693-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fc693-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc693-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-119">-ContainerService</span></span>
<span data-ttu-id="fc693-120">Değişiklikleri içeren bir yerel **kapsayıcı hizmet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc693-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="fc693-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc693-121">-DefaultProfile</span></span>
<span data-ttu-id="fc693-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc693-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc693-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc693-123">-Name</span></span>
<span data-ttu-id="fc693-124">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc693-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="fc693-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc693-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc693-126">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc693-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="fc693-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc693-127">-Confirm</span></span>
<span data-ttu-id="fc693-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc693-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc693-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc693-129">-WhatIf</span></span>
<span data-ttu-id="fc693-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc693-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc693-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc693-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc693-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc693-132">CommonParameters</span></span>
<span data-ttu-id="fc693-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc693-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc693-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc693-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc693-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc693-135">INPUTS</span></span>

### <span data-ttu-id="fc693-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fc693-136">System.String</span></span>

### <span data-ttu-id="fc693-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fc693-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc693-138">OUTPUTS</span></span>

### <span data-ttu-id="fc693-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fc693-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc693-140">NOTES</span></span>

## <span data-ttu-id="fc693-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc693-141">RELATED LINKS</span></span>

[<span data-ttu-id="fc693-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fc693-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="fc693-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="fc693-144">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="fc693-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fc693-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="fc693-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fc693-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


