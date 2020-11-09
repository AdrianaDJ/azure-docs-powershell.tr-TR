---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324787"
---
# <span data-ttu-id="daa8d-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="daa8d-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="daa8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa8d-102">SYNOPSIS</span></span>
<span data-ttu-id="daa8d-103">Konakları alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="daa8d-103">Get or list hosts.</span></span>

## <span data-ttu-id="daa8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daa8d-104">SYNTAX</span></span>

### <span data-ttu-id="daa8d-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="daa8d-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daa8d-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="daa8d-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa8d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="daa8d-107">DESCRIPTION</span></span>
<span data-ttu-id="daa8d-108">Bu cmdlet bir konak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="daa8d-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="daa8d-109">Bu cmdlet, bir konak grubu adı verilmezse, kaynak grubundaki tüm konak gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="daa8d-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="daa8d-110">Bu cmdlet, konak grubu adı veya kaynak grubu adı verilmezse, bir abonelikteki tüm konak gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="daa8d-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="daa8d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daa8d-111">EXAMPLES</span></span>

### <span data-ttu-id="daa8d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="daa8d-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="daa8d-113">Bu komut, bir konak grubu döndürür.</span><span class="sxs-lookup"><span data-stu-id="daa8d-113">This command returns a host group.</span></span>

### <span data-ttu-id="daa8d-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="daa8d-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="daa8d-115">Bu komut, verilen kaynak grubundaki tüm konak gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="daa8d-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="daa8d-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="daa8d-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="daa8d-117">Bu komut, abonelikteki tüm konak gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="daa8d-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="daa8d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daa8d-118">PARAMETERS</span></span>

### <span data-ttu-id="daa8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa8d-119">-DefaultProfile</span></span>
<span data-ttu-id="daa8d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="daa8d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa8d-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="daa8d-121">-InstanceView</span></span>
<span data-ttu-id="daa8d-122">Uygulamanın örnek görünümlerini de listelemek için döndürülen nesneyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="daa8d-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa8d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="daa8d-123">-Name</span></span>
<span data-ttu-id="daa8d-124">Konak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="daa8d-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daa8d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa8d-125">-ResourceGroupName</span></span>
<span data-ttu-id="daa8d-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="daa8d-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daa8d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="daa8d-127">-ResourceId</span></span>
<span data-ttu-id="daa8d-128">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="daa8d-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="daa8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa8d-129">CommonParameters</span></span>
<span data-ttu-id="daa8d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daa8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa8d-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="daa8d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa8d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daa8d-132">INPUTS</span></span>

### <span data-ttu-id="daa8d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="daa8d-133">System.String</span></span>

## <span data-ttu-id="daa8d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daa8d-134">OUTPUTS</span></span>

### <span data-ttu-id="daa8d-135">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="daa8d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="daa8d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daa8d-136">NOTES</span></span>

## <span data-ttu-id="daa8d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daa8d-137">RELATED LINKS</span></span>
