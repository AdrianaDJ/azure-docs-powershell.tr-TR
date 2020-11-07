---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: 9dd2018fe6f84ff4657da799fbcba720e8523bde
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765216"
---
# <span data-ttu-id="3a27c-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="3a27c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a27c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a27c-103">Kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a27c-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a27c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a27c-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a27c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a27c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a27c-106">**Yeni-AzureRmContainerService** cmdlet 'i bir kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a27c-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="3a27c-107">New-AzureRmContainerServiceConfig cmdlet 'ini kullanarak oluşturabileceğiniz bir kapsayıcı hizmeti nesnesi belirtin.</span><span class="sxs-lookup"><span data-stu-id="3a27c-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="3a27c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a27c-108">EXAMPLES</span></span>

### <span data-ttu-id="3a27c-109">Örnek 1: kapsayıcı hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a27c-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="3a27c-110">İlk komut, belirtilen konumda ResourceGroup17 adlı bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a27c-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="3a27c-111">Daha fazla bilgi için New-AzureRmResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="3a27c-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="3a27c-112">İkinci komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3a27c-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3a27c-113">Daha fazla bilgi için New-AzureRmContainerServiceConfig cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="3a27c-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="3a27c-114">Son komutu, $Container depolanan kapsayıcı için bir kapsayıcı hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a27c-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="3a27c-115">Hizmetin adı csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="3a27c-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="3a27c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a27c-116">PARAMETERS</span></span>

### <span data-ttu-id="3a27c-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="3a27c-117">-AsJob</span></span>
<span data-ttu-id="3a27c-118">Iş arka planda RRun cmdlet 'i ve ilerlemeyi izlemek için bir Iş döndürün.</span><span class="sxs-lookup"><span data-stu-id="3a27c-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3a27c-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-119">-ContainerService</span></span>
<span data-ttu-id="3a27c-120">Yeni hizmetin özelliklerini içeren bir kapsayıcı hizmeti nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a27c-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="3a27c-121">**Containerservice** nesnesi edinmek için New-AzureRmContainerServiceConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a27c-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="3a27c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a27c-122">-DefaultProfile</span></span>
<span data-ttu-id="3a27c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a27c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a27c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a27c-124">-Name</span></span>
<span data-ttu-id="3a27c-125">Bu cmdlet 'in oluşturduğu kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a27c-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3a27c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a27c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3a27c-127">Bu cmdlet 'in kapsayıcı hizmeti dağıttığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a27c-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="3a27c-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a27c-128">-Confirm</span></span>
<span data-ttu-id="3a27c-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a27c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a27c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a27c-130">-WhatIf</span></span>
<span data-ttu-id="3a27c-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a27c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a27c-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a27c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a27c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a27c-133">CommonParameters</span></span>
<span data-ttu-id="3a27c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a27c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a27c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a27c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a27c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a27c-136">INPUTS</span></span>

### <span data-ttu-id="3a27c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3a27c-137">System.String</span></span>

### <span data-ttu-id="3a27c-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="3a27c-139">Parametreler: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a27c-139">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="3a27c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a27c-140">OUTPUTS</span></span>

### <span data-ttu-id="3a27c-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="3a27c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a27c-142">NOTES</span></span>

## <span data-ttu-id="3a27c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a27c-143">RELATED LINKS</span></span>

[<span data-ttu-id="3a27c-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="3a27c-145">Yeni-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="3a27c-145">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="3a27c-146">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="3a27c-147">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3a27c-147">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


