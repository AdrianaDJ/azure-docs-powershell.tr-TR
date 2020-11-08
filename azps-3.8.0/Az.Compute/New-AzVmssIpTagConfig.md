---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938564"
---
# <span data-ttu-id="c0ba9-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="c0ba9-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="c0ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ba9-103">Bir VMSS 'nin ağ arabirimi için IP etiket nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="c0ba9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0ba9-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0ba9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ba9-106">**New-AzVmssIpTagConfig** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) ağ arabirimi IÇIN bir IP etiketi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c0ba9-107">Bu cmdlet 'i New-AzVmssIpConfig cmdlet 'in *ıptag* parametresi olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="c0ba9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0ba9-108">EXAMPLES</span></span>

### <span data-ttu-id="c0ba9-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0ba9-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="c0ba9-110">Bu komut, ' FirstPartyUsage ' türü ve ' SQL ' etiketiyle bir IP etiketi yerel nesnesi oluşturur ve bu IP etiketiyle bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="c0ba9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0ba9-111">PARAMETERS</span></span>

### <span data-ttu-id="c0ba9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ba9-112">-DefaultProfile</span></span>
<span data-ttu-id="c0ba9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ba9-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="c0ba9-114">-IpTagType</span></span>
<span data-ttu-id="c0ba9-115">IP etiket türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="c0ba9-116">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c0ba9-116">-Tag</span></span>
<span data-ttu-id="c0ba9-117">Bir IP etiket değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ba9-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0ba9-118">-Confirm</span></span>
<span data-ttu-id="c0ba9-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ba9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ba9-120">-WhatIf</span></span>
<span data-ttu-id="c0ba9-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0ba9-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ba9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ba9-123">CommonParameters</span></span>
<span data-ttu-id="c0ba9-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ba9-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ba9-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0ba9-126">INPUTS</span></span>

### <span data-ttu-id="c0ba9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c0ba9-127">System.String</span></span>

## <span data-ttu-id="c0ba9-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0ba9-128">OUTPUTS</span></span>

### <span data-ttu-id="c0ba9-129">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="c0ba9-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="c0ba9-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0ba9-130">NOTES</span></span>

## <span data-ttu-id="c0ba9-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0ba9-131">RELATED LINKS</span></span>