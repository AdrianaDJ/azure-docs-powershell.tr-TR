---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: a87a11b1e894864593d9558b123b19b6bda06e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752950"
---
# <span data-ttu-id="441d7-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="441d7-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="441d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="441d7-102">SYNOPSIS</span></span>
<span data-ttu-id="441d7-103">Konakları alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="441d7-103">Get or list hosts.</span></span>

## <span data-ttu-id="441d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="441d7-104">SYNTAX</span></span>

### <span data-ttu-id="441d7-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="441d7-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="441d7-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="441d7-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="441d7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="441d7-107">DESCRIPTION</span></span>
<span data-ttu-id="441d7-108">Bu cmdlet bir konak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="441d7-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="441d7-109">Bu cmdlet, bir konak grubu adı verilmezse, kaynak grubundaki tüm konak gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="441d7-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="441d7-110">Bu cmdlet, konak grubu adı veya kaynak grubu adı verilmezse, bir abonelikteki tüm konak gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="441d7-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="441d7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="441d7-111">EXAMPLES</span></span>

### <span data-ttu-id="441d7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="441d7-112">Example 1</span></span>
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

<span data-ttu-id="441d7-113">Bu komut, bir konak grubu döndürür.</span><span class="sxs-lookup"><span data-stu-id="441d7-113">This command returns a host group.</span></span>

### <span data-ttu-id="441d7-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="441d7-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="441d7-115">Bu komut, verilen kaynak grubundaki tüm konak gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="441d7-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="441d7-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="441d7-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="441d7-117">Bu komut, abonelikteki tüm konak gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="441d7-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="441d7-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="441d7-118">PARAMETERS</span></span>

### <span data-ttu-id="441d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441d7-119">-DefaultProfile</span></span>
<span data-ttu-id="441d7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="441d7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="441d7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="441d7-121">-Name</span></span>
<span data-ttu-id="441d7-122">Konak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="441d7-122">The name of the host group.</span></span>

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

### <span data-ttu-id="441d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="441d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="441d7-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="441d7-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="441d7-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="441d7-125">-ResourceId</span></span>
<span data-ttu-id="441d7-126">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="441d7-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="441d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441d7-127">CommonParameters</span></span>
<span data-ttu-id="441d7-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="441d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441d7-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="441d7-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441d7-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="441d7-130">INPUTS</span></span>

### <span data-ttu-id="441d7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="441d7-131">System.String</span></span>

## <span data-ttu-id="441d7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="441d7-132">OUTPUTS</span></span>

### <span data-ttu-id="441d7-133">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="441d7-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="441d7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="441d7-134">NOTES</span></span>

## <span data-ttu-id="441d7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="441d7-135">RELATED LINKS</span></span>
