---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: ee85085f27b7d4b94753b40edc8f6a24630c88d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761296"
---
# <span data-ttu-id="c4432-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="c4432-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="c4432-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4432-102">SYNOPSIS</span></span>
<span data-ttu-id="c4432-103">Bir VMSS 'nin ağ arabirimi için IP etiket nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4432-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="c4432-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4432-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4432-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4432-105">DESCRIPTION</span></span>
<span data-ttu-id="c4432-106">**New-AzVmssIpTagConfig** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) ağ arabirimi IÇIN bir IP etiketi yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4432-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c4432-107">Bu cmdlet 'i New-AzVmssIpConfig cmdlet 'in *ıptag* parametresi olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="c4432-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="c4432-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4432-108">EXAMPLES</span></span>

### <span data-ttu-id="c4432-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4432-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="c4432-110">Bu komut, ' FirstPartyUsage ' türü ve ' SQL ' etiketiyle bir IP etiketi yerel nesnesi oluşturur ve bu IP etiketiyle bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4432-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="c4432-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4432-111">PARAMETERS</span></span>

### <span data-ttu-id="c4432-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4432-112">-DefaultProfile</span></span>
<span data-ttu-id="c4432-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4432-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4432-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="c4432-114">-IpTagType</span></span>
<span data-ttu-id="c4432-115">IP etiket türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4432-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="c4432-116">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c4432-116">-Tag</span></span>
<span data-ttu-id="c4432-117">Bir IP etiket değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4432-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="c4432-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4432-118">-Confirm</span></span>
<span data-ttu-id="c4432-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4432-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4432-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4432-120">-WhatIf</span></span>
<span data-ttu-id="c4432-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4432-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4432-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4432-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4432-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4432-123">CommonParameters</span></span>
<span data-ttu-id="c4432-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4432-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4432-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4432-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4432-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4432-126">INPUTS</span></span>

### <span data-ttu-id="c4432-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c4432-127">System.String</span></span>

## <span data-ttu-id="c4432-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4432-128">OUTPUTS</span></span>

### <span data-ttu-id="c4432-129">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="c4432-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="c4432-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4432-130">NOTES</span></span>

## <span data-ttu-id="c4432-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4432-131">RELATED LINKS</span></span>