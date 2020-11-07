---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940158"
---
# <span data-ttu-id="e3295-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="e3295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3295-102">SYNOPSIS</span></span>
<span data-ttu-id="e3295-103">Kapsayıcı hizmetin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e3295-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3295-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3295-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3295-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3295-105">DESCRIPTION</span></span>
<span data-ttu-id="e3295-106">**Update-AzureRmContainerService** cmdlet 'i, bir kapsayıcı hizmetinin durumunu hizmetin yerel örneğiyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e3295-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="e3295-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3295-107">EXAMPLES</span></span>

### <span data-ttu-id="e3295-108">Örnek 1: kapsayıcı hizmeti güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e3295-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="e3295-109">Bu komut, Get-AzureRmContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="e3295-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="e3295-110">Komut, ardışık düzen işlecini kullanarak bu nesneyi Remove-AzureRmContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="e3295-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="e3295-111">**Remove-AzureRmContainerServiceAgentPoolProfile** , AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3295-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="e3295-112">Komut sonucu Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="e3295-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="e3295-113">**Add-AzureRmContainerServiceAgentPoolProfile** , AgentPool01 adında bir profil ekler ve belirtilen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e3295-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="e3295-114">Komut sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="e3295-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="e3295-115">Geçerli cmdlet, kapsayıcı hizmetini Bu komutta yapılan değişiklikleri yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e3295-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="e3295-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3295-116">PARAMETERS</span></span>

### <span data-ttu-id="e3295-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="e3295-117">-AsJob</span></span>
<span data-ttu-id="e3295-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e3295-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-119">-ContainerService</span></span>
<span data-ttu-id="e3295-120">Değişiklikleri içeren bir yerel **kapsayıcı hizmet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3295-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3295-121">-DefaultProfile</span></span>
<span data-ttu-id="e3295-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3295-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3295-123">-Name</span></span>
<span data-ttu-id="e3295-124">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3295-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3295-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3295-126">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3295-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3295-127">-Confirm</span></span>
<span data-ttu-id="e3295-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3295-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3295-129">-WhatIf</span></span>
<span data-ttu-id="e3295-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3295-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e3295-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3295-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3295-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3295-132">CommonParameters</span></span>
<span data-ttu-id="e3295-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3295-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3295-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3295-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3295-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3295-135">INPUTS</span></span>

### <span data-ttu-id="e3295-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-136">ContainerService</span></span>
<span data-ttu-id="e3295-137">Parametre ' ContainerService ', ardışık düzenin ' ContainerService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e3295-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="e3295-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3295-138">OUTPUTS</span></span>

### <span data-ttu-id="e3295-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e3295-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3295-140">NOTES</span></span>

## <span data-ttu-id="e3295-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3295-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3295-142">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e3295-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e3295-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="e3295-144">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="e3295-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e3295-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="e3295-146">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e3295-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


