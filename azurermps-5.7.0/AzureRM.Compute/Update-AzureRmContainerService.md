---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: 62acfacbafb50f85673b37e802b9d0b0eb4bf66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586768"
---
# <span data-ttu-id="6633c-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6633c-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="6633c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6633c-102">SYNOPSIS</span></span>
<span data-ttu-id="6633c-103">Kapsayıcı hizmetin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6633c-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6633c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6633c-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6633c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6633c-105">DESCRIPTION</span></span>
<span data-ttu-id="6633c-106">**Update-AzureRmContainerService** cmdlet 'i, bir kapsayıcı hizmetinin durumunu hizmetin yerel örneğiyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6633c-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="6633c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6633c-107">EXAMPLES</span></span>

### <span data-ttu-id="6633c-108">Örnek 1: kapsayıcı hizmeti güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6633c-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="6633c-109">Bu komut, Get-AzureRmContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="6633c-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="6633c-110">Komut, ardışık düzen işlecini kullanarak bu nesneyi Remove-AzureRmContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="6633c-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="6633c-111">**Remove-AzureRmContainerServiceAgentPoolProfile** , AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6633c-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="6633c-112">Komut sonucu Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="6633c-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="6633c-113">**Add-AzureRmContainerServiceAgentPoolProfile** , AgentPool01 adında bir profil ekler ve belirtilen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="6633c-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="6633c-114">Komut sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="6633c-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="6633c-115">Geçerli cmdlet, kapsayıcı hizmetini Bu komutta yapılan değişiklikleri yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6633c-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="6633c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6633c-116">PARAMETERS</span></span>

### <span data-ttu-id="6633c-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="6633c-117">-ContainerService</span></span>
<span data-ttu-id="6633c-118">Değişiklikleri içeren bir yerel **kapsayıcı hizmet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6633c-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6633c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6633c-119">-Name</span></span>
<span data-ttu-id="6633c-120">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6633c-120">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="6633c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6633c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6633c-122">Bu cmdlet 'in güncelleştirdiği kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6633c-122">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="6633c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="6633c-123">-Confirm</span></span>
<span data-ttu-id="6633c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6633c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6633c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6633c-125">-WhatIf</span></span>
<span data-ttu-id="6633c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6633c-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6633c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6633c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6633c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6633c-128">CommonParameters</span></span>
<span data-ttu-id="6633c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6633c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6633c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6633c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6633c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6633c-131">INPUTS</span></span>

### <span data-ttu-id="6633c-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6633c-132">None</span></span>
<span data-ttu-id="6633c-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6633c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6633c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6633c-134">OUTPUTS</span></span>

## <span data-ttu-id="6633c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6633c-135">NOTES</span></span>

## <span data-ttu-id="6633c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6633c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6633c-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="6633c-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="6633c-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6633c-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="6633c-139">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6633c-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="6633c-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6633c-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="6633c-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="6633c-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


