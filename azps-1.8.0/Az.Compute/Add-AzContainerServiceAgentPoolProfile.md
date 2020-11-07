---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 4a356af4090fefe25956fb421b0df409e1edd79b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761385"
---
# <span data-ttu-id="e8f8f-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e8f8f-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="e8f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f8f-103">Kapsayıcı hizmet Aracısı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="e8f8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8f8f-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="e8f8f-106">**Add-AzContainerServiceAgentPoolProfile** cmdlet 'i yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="e8f8f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="e8f8f-108">Örnek 1: profil ekleme</span><span class="sxs-lookup"><span data-stu-id="e8f8f-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="e8f8f-109">Bu komut, yerel kapsayıcı hizmet nesnesine kapsayıcı hizmet Aracısı havuzu profili ekler.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="e8f8f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8f8f-110">PARAMETERS</span></span>

### <span data-ttu-id="e8f8f-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="e8f8f-111">-ContainerService</span></span>
<span data-ttu-id="e8f8f-112">Bu cmdlet 'in bir aracı havuz profili eklediği kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="e8f8f-113">**Containerservice** nesnesi edinmek Için, [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8f-114">-Sayı</span><span class="sxs-lookup"><span data-stu-id="e8f8f-114">-Count</span></span>
<span data-ttu-id="e8f8f-115">Kapsayıcıları barındıran aracıların sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="e8f8f-116">Bu parametre için kabul edilebilir değerler: 1 ile 100 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="e8f8f-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f8f-118">-DefaultProfile</span></span>
<span data-ttu-id="e8f8f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8f8f-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="e8f8f-120">-DnsPrefix</span></span>
<span data-ttu-id="e8f8f-121">Bu aracı havuzunun tam nitelikli etki alanı adını oluşturmak için bu cmdlet 'in kullandığı DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8f8f-122">-Name</span></span>
<span data-ttu-id="e8f8f-123">Aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="e8f8f-124">Bu değer, abonelik ve kaynak grubu bağlamında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8f-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="e8f8f-125">-VmSize</span></span>
<span data-ttu-id="e8f8f-126">Aracıların sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8f8f-127">-Confirm</span></span>
<span data-ttu-id="e8f8f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f8f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f8f-129">-WhatIf</span></span>
<span data-ttu-id="e8f8f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8f8f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f8f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f8f-132">CommonParameters</span></span>
<span data-ttu-id="e8f8f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8f8f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f8f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f8f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f8f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8f8f-135">INPUTS</span></span>

### <span data-ttu-id="e8f8f-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e8f8f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="e8f8f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f8f-137">System.String</span></span>

### <span data-ttu-id="e8f8f-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e8f8f-138">System.Int32</span></span>

## <span data-ttu-id="e8f8f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8f8f-139">OUTPUTS</span></span>

### <span data-ttu-id="e8f8f-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e8f8f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e8f8f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8f8f-141">NOTES</span></span>

## <span data-ttu-id="e8f8f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8f8f-142">RELATED LINKS</span></span>

[<span data-ttu-id="e8f8f-143">Yeni-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="e8f8f-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="e8f8f-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e8f8f-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
