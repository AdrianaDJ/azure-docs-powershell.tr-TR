---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 9d8afa31d296e62c75b869bd93e6f96aadf82328
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761361"
---
# <span data-ttu-id="3631f-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3631f-101">Get-AzContainerService</span></span>

## <span data-ttu-id="3631f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3631f-102">SYNOPSIS</span></span>
<span data-ttu-id="3631f-103">Kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="3631f-103">Gets a container service.</span></span>

## <span data-ttu-id="3631f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3631f-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3631f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3631f-105">DESCRIPTION</span></span>
<span data-ttu-id="3631f-106">**Get-AzContainerService** cmdlet 'i bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="3631f-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="3631f-107">Ana ve aracının tam nitelikli etki alanı adını içeren, bölge, ana ve aracılar sayısı gibi bir kapsayıcı hizmetin özelliklerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3631f-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="3631f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3631f-108">EXAMPLES</span></span>

### <span data-ttu-id="3631f-109">Örnek 1: kapsayıcı hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="3631f-109">Example 1: Get a container service</span></span>
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

<span data-ttu-id="3631f-110">Bu komut, CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="3631f-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="3631f-111">Örnek 2: tüm kapsayıcı hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="3631f-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="3631f-112">Bu komut, abonelikteki tüm kapsayıcı hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3631f-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="3631f-113">Örnek 3: kaynak grubundaki tüm kapsayıcı hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="3631f-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="3631f-114">Bu komut, ResourceGroup17 'deki tüm kapsayıcı hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3631f-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="3631f-115">Örnek 4: filtre kullanarak tüm kapsayıcı hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="3631f-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="3631f-116">Bu komut, "CSResourceGroup1" ile başlayan tüm kapsayıcı hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3631f-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="3631f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3631f-117">PARAMETERS</span></span>

### <span data-ttu-id="3631f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3631f-118">-DefaultProfile</span></span>
<span data-ttu-id="3631f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3631f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3631f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3631f-120">-Name</span></span>
<span data-ttu-id="3631f-121">Bu cmdlet 'in aldığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3631f-121">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3631f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3631f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3631f-123">Bu cmdlet 'in aldığı kapsayıcı hizmetinin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3631f-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3631f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3631f-124">CommonParameters</span></span>
<span data-ttu-id="3631f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3631f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3631f-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3631f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3631f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3631f-127">INPUTS</span></span>

### <span data-ttu-id="3631f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3631f-128">System.String</span></span>

## <span data-ttu-id="3631f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3631f-129">OUTPUTS</span></span>

### <span data-ttu-id="3631f-130">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="3631f-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="3631f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3631f-131">NOTES</span></span>

## <span data-ttu-id="3631f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3631f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3631f-133">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3631f-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="3631f-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3631f-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="3631f-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3631f-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


