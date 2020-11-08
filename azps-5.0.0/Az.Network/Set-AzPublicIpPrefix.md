---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278807"
---
# <span data-ttu-id="43075-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="43075-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="43075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43075-102">SYNOPSIS</span></span>
<span data-ttu-id="43075-103">Var olan Publicıpprefix için etiketleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="43075-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="43075-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43075-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43075-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43075-105">DESCRIPTION</span></span>
<span data-ttu-id="43075-106">**Set-AzPublicIpPrefix** cmdlet 'ı genel IP önekinin etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="43075-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="43075-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43075-107">EXAMPLES</span></span>

### <span data-ttu-id="43075-108">Genel IP öneki için etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="43075-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="43075-109">İlk komut mevcut bir genel IP önekini alır, ikinci komut Etiketler özelliğini ayarlar ve üçüncü komut varolan nesneyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="43075-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="43075-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43075-110">PARAMETERS</span></span>

### <span data-ttu-id="43075-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="43075-111">-AsJob</span></span>
<span data-ttu-id="43075-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="43075-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43075-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43075-113">-DefaultProfile</span></span>
<span data-ttu-id="43075-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43075-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43075-115">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="43075-115">-PublicIpPrefix</span></span>
<span data-ttu-id="43075-116">Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="43075-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43075-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="43075-117">-Confirm</span></span>
<span data-ttu-id="43075-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43075-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43075-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43075-119">-WhatIf</span></span>
<span data-ttu-id="43075-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43075-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43075-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43075-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43075-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43075-122">CommonParameters</span></span>
<span data-ttu-id="43075-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43075-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43075-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43075-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43075-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43075-125">INPUTS</span></span>

### <span data-ttu-id="43075-126">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="43075-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="43075-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43075-127">OUTPUTS</span></span>

### <span data-ttu-id="43075-128">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="43075-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="43075-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43075-129">NOTES</span></span>

## <span data-ttu-id="43075-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43075-130">RELATED LINKS</span></span>

[<span data-ttu-id="43075-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="43075-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="43075-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="43075-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="43075-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="43075-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
