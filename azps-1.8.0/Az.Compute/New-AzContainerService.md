---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: cd988a78962e1603be42e867fbc27bd0e58ff69c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917387"
---
# <span data-ttu-id="aed96-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-101">New-AzContainerService</span></span>

## <span data-ttu-id="aed96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed96-102">SYNOPSIS</span></span>
<span data-ttu-id="aed96-103">Kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aed96-103">Creates a container service.</span></span>

## <span data-ttu-id="aed96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aed96-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aed96-105">DESCRIPTION</span></span>
<span data-ttu-id="aed96-106">**New-AzContainerService** cmdlet 'i bir kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aed96-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="aed96-107">New-AzContainerServiceConfig cmdlet 'ini kullanarak oluşturabileceğiniz bir kapsayıcı hizmeti nesnesi belirtin.</span><span class="sxs-lookup"><span data-stu-id="aed96-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="aed96-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aed96-108">EXAMPLES</span></span>

### <span data-ttu-id="aed96-109">Örnek 1: kapsayıcı hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="aed96-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="aed96-110">İlk komut, belirtilen konumda ResourceGroup17 adlı bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aed96-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="aed96-111">Daha fazla bilgi için New-AzResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="aed96-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="aed96-112">İkinci komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aed96-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="aed96-113">Daha fazla bilgi için New-AzContainerServiceConfig cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="aed96-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="aed96-114">Son komutu, $Container depolanan kapsayıcı için bir kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aed96-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="aed96-115">Hizmetin adı csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="aed96-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="aed96-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aed96-116">PARAMETERS</span></span>

### <span data-ttu-id="aed96-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="aed96-117">-AsJob</span></span>
<span data-ttu-id="aed96-118">Iş arka planda RRun cmdlet 'i ve ilerlemeyi izlemek için bir Iş döndürün.</span><span class="sxs-lookup"><span data-stu-id="aed96-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aed96-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-119">-ContainerService</span></span>
<span data-ttu-id="aed96-120">Yeni hizmetin özelliklerini içeren bir kapsayıcı hizmeti nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aed96-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="aed96-121">**Containerservice** nesnesi edinmek için New-AzContainerServiceConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aed96-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="aed96-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed96-122">-DefaultProfile</span></span>
<span data-ttu-id="aed96-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aed96-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed96-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="aed96-124">-Name</span></span>
<span data-ttu-id="aed96-125">Bu cmdlet 'in oluşturduğu kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aed96-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="aed96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed96-126">-ResourceGroupName</span></span>
<span data-ttu-id="aed96-127">Bu cmdlet 'in kapsayıcı hizmeti dağıttığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aed96-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="aed96-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="aed96-128">-Confirm</span></span>
<span data-ttu-id="aed96-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aed96-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed96-130">-WhatIf</span></span>
<span data-ttu-id="aed96-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aed96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aed96-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aed96-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed96-133">CommonParameters</span></span>
<span data-ttu-id="aed96-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aed96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed96-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed96-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed96-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aed96-136">INPUTS</span></span>

### <span data-ttu-id="aed96-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aed96-137">System.String</span></span>

### <span data-ttu-id="aed96-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="aed96-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aed96-139">OUTPUTS</span></span>

### <span data-ttu-id="aed96-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="aed96-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aed96-141">NOTES</span></span>

## <span data-ttu-id="aed96-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aed96-142">RELATED LINKS</span></span>

[<span data-ttu-id="aed96-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="aed96-144">Yeni-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="aed96-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="aed96-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="aed96-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aed96-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


