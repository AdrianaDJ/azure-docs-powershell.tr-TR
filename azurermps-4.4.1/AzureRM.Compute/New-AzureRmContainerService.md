---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: d908f99e9a1eaa191b45ed08cdb69ebf40b21756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762072"
---
# <span data-ttu-id="8f177-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f177-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="8f177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f177-102">SYNOPSIS</span></span>
<span data-ttu-id="8f177-103">Kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f177-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f177-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f177-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f177-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f177-105">DESCRIPTION</span></span>
<span data-ttu-id="8f177-106">**Yeni-AzureRmContainerService** cmdlet 'i bir kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f177-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="8f177-107">New-AzureRmContainerServiceConfig cmdlet 'ini kullanarak oluşturabileceğiniz bir kapsayıcı hizmeti nesnesi belirtin.</span><span class="sxs-lookup"><span data-stu-id="8f177-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="8f177-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f177-108">EXAMPLES</span></span>

### <span data-ttu-id="8f177-109">Örnek 1: kapsayıcı hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="8f177-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="8f177-110">İlk komut, belirtilen konumda ResourceGroup17 adlı bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f177-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="8f177-111">Daha fazla bilgi için New-AzureRmResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="8f177-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="8f177-112">İkinci komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8f177-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8f177-113">Daha fazla bilgi için New-AzureRmContainerServiceConfig cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="8f177-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="8f177-114">Son komutu, $Container depolanan kapsayıcı için bir kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f177-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="8f177-115">Hizmetin adı csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="8f177-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="8f177-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f177-116">PARAMETERS</span></span>

### <span data-ttu-id="8f177-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="8f177-117">-ContainerService</span></span>
<span data-ttu-id="8f177-118">Yeni hizmetin özelliklerini içeren bir kapsayıcı hizmeti nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f177-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="8f177-119">**Containerservice** nesnesi edinmek için New-AzureRmContainerServiceConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8f177-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f177-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f177-120">-DefaultProfile</span></span>
<span data-ttu-id="8f177-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f177-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f177-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f177-122">-Name</span></span>
<span data-ttu-id="8f177-123">Bu cmdlet 'in oluşturduğu kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f177-123">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f177-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f177-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f177-125">Bu cmdlet 'in kapsayıcı hizmeti dağıttığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f177-125">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="8f177-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f177-126">-Confirm</span></span>
<span data-ttu-id="8f177-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f177-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f177-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f177-128">-WhatIf</span></span>
<span data-ttu-id="8f177-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f177-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8f177-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f177-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f177-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f177-131">CommonParameters</span></span>
<span data-ttu-id="8f177-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f177-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f177-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f177-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f177-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f177-134">INPUTS</span></span>

## <span data-ttu-id="8f177-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f177-135">OUTPUTS</span></span>

## <span data-ttu-id="8f177-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f177-136">NOTES</span></span>

## <span data-ttu-id="8f177-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f177-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f177-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f177-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="8f177-139">Yeni-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8f177-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="8f177-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f177-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="8f177-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f177-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)

