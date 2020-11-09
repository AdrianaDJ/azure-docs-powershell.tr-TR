---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324790"
---
# <span data-ttu-id="e2148-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="e2148-101">Get-AzHost</span></span>

## <span data-ttu-id="e2148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2148-102">SYNOPSIS</span></span>
<span data-ttu-id="e2148-103">Konakları alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="e2148-103">Get or list hosts.</span></span>

## <span data-ttu-id="e2148-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2148-104">SYNTAX</span></span>

### <span data-ttu-id="e2148-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2148-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2148-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="e2148-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2148-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2148-107">DESCRIPTION</span></span>
<span data-ttu-id="e2148-108">Bu cmdlet, konak grubundaki bir ana bilgisayarı alır.</span><span class="sxs-lookup"><span data-stu-id="e2148-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="e2148-109">Bu cmdlet, bir ana bilgisayar adı verilmemişse tüm ana bilgisayarları da listeler.</span><span class="sxs-lookup"><span data-stu-id="e2148-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="e2148-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2148-110">EXAMPLES</span></span>

### <span data-ttu-id="e2148-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2148-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="e2148-112">Bu komut bir ana bilgisayar döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2148-112">This command returns a host.</span></span>

### <span data-ttu-id="e2148-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e2148-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="e2148-114">Bu komut, bir ana bilgisayarın örnek görünümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2148-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="e2148-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e2148-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="e2148-116">Bu komut, verilen konak grubundaki tüm Konakları döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2148-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="e2148-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2148-117">PARAMETERS</span></span>

### <span data-ttu-id="e2148-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2148-118">-DefaultProfile</span></span>
<span data-ttu-id="e2148-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2148-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2148-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="e2148-120">-HostGroupName</span></span>
<span data-ttu-id="e2148-121">Konak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e2148-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2148-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="e2148-122">-InstanceView</span></span>
<span data-ttu-id="e2148-123">Bu cmdlet 'in yalnızca ana bilgisayarın örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2148-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

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

### <span data-ttu-id="e2148-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2148-124">-Name</span></span>
<span data-ttu-id="e2148-125">Ana bilgisayarın adı.</span><span class="sxs-lookup"><span data-stu-id="e2148-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2148-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2148-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2148-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e2148-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2148-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e2148-128">-ResourceId</span></span>
<span data-ttu-id="e2148-129">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e2148-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2148-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2148-130">CommonParameters</span></span>
<span data-ttu-id="e2148-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2148-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2148-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2148-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2148-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2148-133">INPUTS</span></span>

### <span data-ttu-id="e2148-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e2148-134">System.String</span></span>

## <span data-ttu-id="e2148-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2148-135">OUTPUTS</span></span>

### <span data-ttu-id="e2148-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHost</span><span class="sxs-lookup"><span data-stu-id="e2148-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="e2148-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2148-137">NOTES</span></span>

## <span data-ttu-id="e2148-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2148-138">RELATED LINKS</span></span>
