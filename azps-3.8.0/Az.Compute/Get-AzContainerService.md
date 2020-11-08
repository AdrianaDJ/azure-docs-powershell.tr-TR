---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098919"
---
# <span data-ttu-id="d6216-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d6216-101">Get-AzContainerService</span></span>

## <span data-ttu-id="d6216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6216-102">SYNOPSIS</span></span>
<span data-ttu-id="d6216-103">Kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="d6216-103">Gets a container service.</span></span>

## <span data-ttu-id="d6216-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6216-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6216-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6216-105">DESCRIPTION</span></span>
<span data-ttu-id="d6216-106">**Get-AzContainerService** cmdlet 'i bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="d6216-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="d6216-107">Ana ve aracının tam nitelikli etki alanı adını içeren, bölge, ana ve aracılar sayısı gibi bir kapsayıcı hizmetin özelliklerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6216-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="d6216-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6216-108">EXAMPLES</span></span>

### <span data-ttu-id="d6216-109">Örnek 1: kapsayıcı hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="d6216-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="d6216-110">Bu komut, CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="d6216-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="d6216-111">Örnek 2: tüm kapsayıcı hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="d6216-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="d6216-112">Bu komut, abonelikteki tüm kapsayıcı hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d6216-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="d6216-113">Örnek 3: kaynak grubundaki tüm kapsayıcı hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="d6216-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="d6216-114">Bu komut, ResourceGroup17 'deki tüm kapsayıcı hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d6216-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="d6216-115">Örnek 4: filtre kullanarak tüm kapsayıcı hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="d6216-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="d6216-116">Bu komut, "CSResourceGroup1" ile başlayan tüm kapsayıcı hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d6216-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="d6216-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6216-117">PARAMETERS</span></span>

### <span data-ttu-id="d6216-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6216-118">-DefaultProfile</span></span>
<span data-ttu-id="d6216-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6216-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6216-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6216-120">-Name</span></span>
<span data-ttu-id="d6216-121">Bu cmdlet 'in aldığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6216-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d6216-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6216-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6216-123">Bu cmdlet 'in aldığı kapsayıcı hizmetinin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6216-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d6216-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6216-124">CommonParameters</span></span>
<span data-ttu-id="d6216-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6216-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6216-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d6216-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6216-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6216-127">INPUTS</span></span>

### <span data-ttu-id="d6216-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d6216-128">System.String</span></span>

## <span data-ttu-id="d6216-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6216-129">OUTPUTS</span></span>

### <span data-ttu-id="d6216-130">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d6216-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d6216-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6216-131">NOTES</span></span>

## <span data-ttu-id="d6216-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6216-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6216-133">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d6216-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="d6216-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d6216-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="d6216-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d6216-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)

